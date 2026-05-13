---
title: Manual Installation Guide for the New Hosted Mall Script (trans version) for NAVER Ads Web Conversion Tracking
layout: post
lesson: 3
---
------


# 1. Overview
## 1.1. Target Services and Purpose of This Document
This document provides guidance for advertisers using a hosted mall who want to install additional new-script (trans version) conversion types on their site, beyond the conversion types that are automatically applied by the hosted mall system.

The conversion types currently applied automatically by each hosted mall system through the new script (trans version) are as follows.<br>
 . Cafe24: purchase completion (`purchase`), product detail view (`view_product`), add to cart (`add_to_cart`), begin checkout (`begin_checkout`) (all 4 conversion types occur when configured)<br>
 . MakeShop: purchase completion (`purchase`), sign-up completion (`sign_up`), product detail view (`view_product`), add to cart (`add_to_cart`), add product to wishlist (`add_to_wishlist`), begin checkout (`begin_checkout`). (The conversion types to use can be configured through the Admin UI.)<br>

Automatic system-applied conversions will also be expanded to other hosted malls. We will notify you through announcements when they are applied.

## 2. Cafe24 Installation Method
For Cafe24, the conversion types automatically applied by the system through the new script (trans version) are as follows.<br>
. Cafe24: purchase completion (`purchase`), product detail view (`view_product`), add to cart (`add_to_cart`), begin checkout (`begin_checkout`) (all 4 conversion types occur when configured. There is currently no way to configure only selected conversions, but this is planned for a future release.)

If you want to generate conversion types other than the above, you can manually insert a conversion script into the Cafe24 design skin to generate additional conversion types.

Please proceed with the following steps. <br>
(To make the explanation easier to understand, this guide uses the example of inserting a conversion script for `sign_up`.)

#### STEP 00. Check the NAVER common authentication key, which is the site identifier

When you apply for conversion analysis by site/business channel in the NAVER Search Ad or NAVER Performance Display Ad platform, a site/business-channel identifier (= NAVER common key, na_account_id) is assigned. This identifier (= NAVER common key, na_account_id) is issued 1-2 business days after applying for the log analysis service, and you can check the issued NAVER common key in the following ways.

(i) For NAVER Search Ad<br>
. In the Search Ad system, go to [Tools > Premium Log Analysis], click the [Overall Service Usage Status] tab, and check the value in the [NAVER Common Key] column.

(ii) For NAVER Performance Display Ad<br>
. In the ad management system, go to [Tools > Conversion Tracking Management], select the site, and check it in the window that shows detailed information.

(iii) Common method (check by email)<br>
. You can check the email sent on the next business day after applying for the log analysis service to the email address entered during the application or to the advertiser email address.

#### STEP 01. Log in to the Cafe24 Admin screen and click the 'Design (PC/Mobile)' menu

![Cafe24_01]({{"/assets/img/03_ecom_ptg_cafe24_step01.png"| relative_url}})

#### STEP 02. Click the 'Edit Design' button for the design skin you want to use
![Cafe24_02]({{"/assets/img/03_ecom_ptg_cafe24_step02.png"| relative_url}})

#### STEP 03. Insert the conversion script on the screen where the conversion action is completed.
Find the screen where the conversion action you want to insert is completed. (For sign-up completion, find `Member > Sign-up Result (join_result.html)`.)<br>
Insert the script at the very bottom of the `HTML` insertion screen on the right.


![Cafe24_03]({{"/assets/img/03_ecom_ptg_cafe24_step03.png"| relative_url}})

The copyable script from the image above is as follows.

```js
<!-- Start additional script block for NAVER conversion tracking -->
<script type="text/javascript">
if (window.wcs) {
    if(!wcs_add) var wcs_add = {};
    // (2) Set the identifier for each site
    wcs_add["wa"] = "s_OOOOOO"; // Site identifier (= NAVER common key, na_account_id). Enter the value for each site.
    
    // trans conversion log
    var _conv = {};
    _conv.type = 'sign_up'; // Enter the string that matches the conversion type you want to use. Example) sign-up: sign_up
    wcs.trans(_conv);
}
</script>
<!-- End additional script block for NAVER conversion tracking -->
```

※ Note<br>
For the full list of strings by conversion type, see the link below.<br>
[2.4.2. Conversion Event Types and Property Descriptions]({{"/pages/01_script_guide_wcstrans/#242-conversion-event-types-and-property-descriptions"| relative_url}})

#### STEP 04. Click the Save button.
Click the 'Save' button to apply the skin screen changes.<br>
![Cafe24_04]({{"/assets/img/03_ecom_ptg_cafe24_step04.png"| relative_url}})

------

Version: 20240718_01
