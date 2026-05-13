---
title: Hosted Mall Setup Guide for NAVER Ads Web Conversion Tracking
layout: post
lesson: 2
---
------


# 1. Overview
## 1.1. Target Services and Purpose of This Document
This document provides a setup guide for advertisers using hosted mall sites partnered with NAVER, so they can use NAVER Search Ad (SA) Premium Log Analysis and NAVER Performance Display Ad conversion tracking services.

## 1.2. NAVER Partner Hosted Malls
There are currently 5 hosted malls partnered with NAVER, as follows.<br>
. Cafe24 <br>
. MakeShop <br>
. Godomall <br>
. Wisa <br>
. WhoisMall <br>

-------------

# 2. NAVER Ads Conversion Analysis Setup Guide by Hosted Mall

## 2.0. Checking the NAVER Common Authentication Key

When you apply for conversion analysis by site/business channel in the NAVER Search Ad or NAVER Performance Display Ad platform, a site/business-channel identifier (= NAVER common key, na_account_id) is assigned.
This identifier (= NAVER common key, na_account_id) is issued 1-2 business days after applying for the log analysis service, and you can check the issued NAVER common key in the following ways.

(i) For NAVER Search Ad<br>
. In the Search Ad system, go to [Tools > Premium Log Analysis], click the [Overall Service Usage Status] tab, and check the value in the [NAVER Common Key] column.
 
(ii) For NAVER Performance Display Ad<br>
 . In the ad management system, go to [Tools > Conversion Tracking Management], select the site, and check it in the window that shows detailed information.
 
(iii) Common method (check by email)<br>
 . You can check the email sent on the next business day after applying for the log analysis service to the email address entered during the application or to the advertiser email address.

## 2.1. Cafe24

In Cafe24, configuring the hosted mall Admin UI as shown below completes the setup for generating 4 conversion types (`purchase completion`, `product detail view`, `add to cart`, `begin checkout`).<br>
(Until Tuesday, July 9, 2024, only `purchase completion` occurred. From Wednesday, July 10, 2024, all 4 conversion types (`purchase completion`, `product detail view`, `add to cart`, `begin checkout`) occur in bulk.)

The setup method is as follows.

① Check the NAVER common authentication key.

② Log in to the Cafe24 Admin ( https://eclogin.cafe24.com/Shop/ )

③ Sales Channels ▶ NAVER ▶ NAVER Pay Settings ▶ NAVER Common Authentication Key Settings ▶ Enter NAVER Common Authentication Key ▶ Register

![Cafe24_01]({{"/assets/img/cafe24_01.png"| relative_url}}){:width="150"}

If you have related questions, please contact us through the channels below. <br>
 . Customer Center (phone): 1877-7035 <br>
 . Channel Talk (chat) consultation: [https://navercts.channel.io/home](https://navercts.channel.io/home) <br>
 . Public email: navercts@nhndata.com <br>

※ Note <br>
 . Among the 4 conversion types generated when configured from Wednesday, July 10, 2024 (`purchase completion`, `product detail view`, `add to cart`, `begin checkout`), a feature for selecting only some of them is not yet provided.<br> We will provide separate guidance later when a partial-selection feature becomes available. <br>
 . From the Wednesday, July 10, 2024 ad reports, `add to cart` conversions will also appear in reports in addition to `purchase completion`. (Note: `product detail view` and `begin checkout` conversions are not displayed in reports.)<br>

### ※ Help for Cafe24 Hosted Mall
Q1) I use Cafe24 hosted mall. Since Wednesday, July 10, 2024, `add to cart` conversions have been collected in my ad reports. Why is this happening?<br>
A) For Cafe24 hosted mall, when NAVER Ads conversion tracking is configured, all `4 conversions` (`purchase completion`, `add to cart`, `product detail view`, `begin checkout`) occur from Wednesday, July 10, 2024.<br>
(Among these, `purchase completion` and `add to cart` conversions appear in reports, while `product detail view` and `begin checkout` do not appear in reports.)<br>
Currently, a feature for selecting only some of these `4 conversions` is not yet provided.<br>
We are discussing a feature with Cafe24 that would allow only selected conversions, and we will notify you through an announcement when it is improved.<br>
As previously announced, the guidance was as follows. Please refer to it.<br>
<br>
■ (Related notice) [Re-announcement] Notice of Changes to the Conversion Tracking Service (7/10 update) (2024. 07. 01.)<br>
https://ads.naver.com/notice/16141?searchValue=&page=1<br>
<br>
※ Please note<br>
 -  Cafe24: applied sequentially on Wednesday, July 10, 2024 and Monday, July 15, 2024
       - Among the new script conversion types, `purchase completion`, `product detail view`, `add to cart`, and `begin checkout` are automatically installed.
       - Advertisers using Cafe24 can check `add to cart` conversions in reports from the above timing, in addition to `purchase completion`.
       - Note. `Product detail view` and `begin checkout` are conversion types that are not provided in reports.

Q2) Can I remove the `add to cart` conversion that occurs in Cafe24 hosted mall?<br>
A) For the `4 conversions` (`purchase completion`, `add to cart`, `product detail view`, `begin checkout`) that occur in Cafe24 hosted mall from Wednesday, July 10, 2024, a feature for selecting only some of them is not yet provided. <br>
We are discussing a feature with Cafe24 that would allow only selected conversions, and we will notify you through an announcement when it is improved.<br>
Until this feature is provided, you can check reports by conversion type using the report viewing features in the ad report (Search Ad: `Reports > Multidimensional Report > Conversion`, `Reports > Bulk Download Report > Bulk Report Download > Conversion-Related Report`; Performance Display Ad: `Dashboard` or `Performance Report > Add Columns > Check Add to Cart Count`). <br>

Q3) In Cafe24 hosted mall, I have conversion counts, but conversion revenue is not visible. Is this an error? <br>
A) In Cafe24 hosted mall, all `4 conversions` (`purchase completion`, `add to cart`, `product detail view`, `begin checkout`) occur. Among these, the conversions shown in reports are `purchase completion` and `add to cart`. `Purchase completion` has conversion revenue, but `add to cart` has conversion revenue of 0 KRW. If only `add to cart` conversions occurred, you will see conversion counts but conversion revenue will appear as 0 KRW. If you use a report that can be viewed by conversion type (※), you should be able to confirm that only `add to cart` conversions occurred without `purchase completion`.  <br>
 <br>
※ [Reference] Reports that can be viewed by conversion type <br>
 . Search Ad: `Reports > Multidimensional Report > Conversion`, `Reports > Bulk Download Report > Bulk Report Download > Conversion-Related Report` <br>
 . Performance Display Ad: `Dashboard` or `Performance Report > Add Columns > Check Add to Cart Count` <br>


## 2.2. MakeShop

In MakeShop, the current conversion type `purchase completion` is completed by configuring it in the hosted mall Admin UI. 
The setup method is as follows.

① Check the NAVER common authentication key.

② Log in to the MakeShop Admin.

③ Integration Management ▶ (left menu `Ad Integration`) NAVER Service Basic Settings ▶ Enter the common authentication key in the `Common Authentication Key` field and click the duplicate check button.

④ NAVER Inflow Route Benefit Script Settings: check `I agree` for script installation consent.

⑤ In the NAVER Search Ad Premium Log Analysis conversion data collection checkbox area, check the conversion types you want to use.<br>
(Note: Starting Tuesday, July 16, 2024, the selectable conversion types increased to 6. `Product detail view` and `begin checkout` conversions are not displayed in reports.)

⑥ Click the `Save` button at the very bottom.

![MakeShop_04]({{"/assets/img/makeshop_04.png"| relative_url}}){:width="150"}


If you have related questions, please contact us through the channels below. <br>

 . Customer Center (phone): 1877-7035 <br>
 . Channel Talk (chat) consultation: [https://navercts.channel.io/home](https://navercts.channel.io/home) <br>
 . Public email: navercts@nhndata.com <br>

## 2.3. Godomall eNamu
In Godomall (eNamu), the current conversion type `purchase completion` is completed by configuring it in the hosted mall Admin UI. 
The setup method is as follows.

① Check the NAVER common authentication key.

② Log in to the Godomall Admin.

③ Marketing ▶ NAVER Shopping ▶ NAVER Shopping Settings ▶ Enter the NAVER common authentication key in the NAVER Common Authentication Key field under Common Inflow Script Settings, then save the settings information.

![Godomall_eNamu_01]({{"/assets/img/godomall_enamu_01.png"| relative_url}})

④ Use status: check `Use`.

⑤ CPA order collection consent status: check `Agree`.

⑥ Save settings information.

![Godomall_eNamu_02]({{"/assets/img/godomall_enamu_02.png"| relative_url}})

To use conversion types other than `purchase completion` (sign-up, add to cart, application/reservation, etc.), you must manually insert the script into skins or similar areas provided by the hosted mall. 
For manual script insertion, contact NHN Data, the official vendor for NAVER Ads conversion analysis scripts, and they will support installation and testing. Please contact the channels below.

 . Customer Center (phone): 1877-7035 <br>
 . Channel Talk (chat) consultation: [https://navercts.channel.io/home](https://navercts.channel.io/home) <br>
 . Public email: navercts@nhndata.com <br>

## 2.4. Godomall 5
Godomall 5 provides 5 conversion types (`purchase completion`, `product detail view`, `product wishlist`, `add to cart`, `begin checkout`) (from 6 PM on Thursday, December 5, 2024).<br>
The setup method in the Godomall Admin UI is as follows.  

※ Note <br>
  . A feature for generating only some of the total 5 conversions is not yet provided.

① Check the NAVER common authentication key.

② Log in to the Godomall Admin.

③ `Marketing` ▶ `NAVER Shopping` ▶ `Common Inflow Script Settings`

④ Use status: check `Use`, enter the NAVER common authentication key in the `NAVER Common Authentication Key` field, then save.

![Godomall5_01]({{"/assets/img/godomall5_01.png"| relative_url}})

⑤ In `Marketing` ▶ `NAVER Shopping` ▶ `NAVER Shopping Settings`, check `Use` for `Use Status`, check `Use` for `CPA Order Collection Consent Status`, then save.

![Godomall5_02]({{"/assets/img/godomall5_02.png"| relative_url}})

### ■ New-Version Application Guide for Existing Godomall 5 Users
If you have previously configured NAVER Search Ad conversion tracking in Godomall 5 before Thursday, December 5, 2024, or are currently using it, you can upgrade to the new script version (V2) by configuring it as follows.

※ Note <br>
  . When you upgrade to the new script version, in addition to the existing `purchase completion` conversion event, 4 more conversion events occur: `product detail view`, `product wishlist`, `add to cart`, and `begin checkout`. Among these, `product wishlist` and `add to cart` conversion events are also shown in reports. This may increase the number of conversions shown in reports compared with before the upgrade.<br>
  . After upgrading once to the new script version (V2), you cannot revert to the old version. Please keep this in mind when using it.<br>
  . A feature for generating only some of the total 5 conversions is not yet provided. <br>

① Access the Godomall Admin and log in as an administrator.

② Go to `Marketing` ▶ `NAVER Shopping` ▶ `Common Inflow Script Settings`.

③ Click the `Switch to Common Inflow Script Settings v2` button. (Complete)

![Godomall5_03]({{"/assets/img/godomall5_241205_01.jpg"| relative_url}})

If you have related questions, please contact us through the channels below. <br>

 . Customer Center (phone): 1877-7035 <br>
 . Channel Talk (chat) consultation: [https://navercts.channel.io/home](https://navercts.channel.io/home) <br>
 . Public email: navercts@nhndata.com <br>

## 2.5. Wisa
In Wisa, the current conversion type `purchase completion` is completed by configuring it in the hosted mall Admin UI. 
The setup method is as follows.

① Check the NAVER common authentication key.

② Log in to the Wisa Admin.

③ Advertising Marketing ▶ Integration Settings ▶ Enter the NAVER common authentication key in the AccountID field of NAVER CPA Settings.

④ CPA service use: check `Use`.

⑤ Confirm.

![Wisa_01]({{"/assets/img/wisa_01.png"| relative_url}})

To use conversion types other than `purchase completion` (sign-up, add to cart, application/reservation, etc.), you must manually insert the script into skins or similar areas provided by the hosted mall. 
For manual script insertion, contact NHN Data, the official vendor for NAVER Ads conversion analysis scripts, and they will support installation and testing. Please contact the channels below.

 . Customer Center (phone): 1877-7035 <br>
 . Channel Talk (chat) consultation: [https://navercts.channel.io/home](https://navercts.channel.io/home) <br>
 . Public email: navercts@nhndata.com <br>

## 2.6. WhoisMall
In WhoisMall, the current conversion type `purchase completion` is completed by configuring it in the hosted mall Admin UI. 
The setup method is as follows.

① Check the NAVER common authentication key.

② Log in to the WhoisMall Admin.

③ Add-on Services ▶ NAVER Service Integration ▶ Enter the NAVER common authentication key in the NAVER Common Authentication Key field under NAVER Common Inflow Settings.

④ Check NAVER service usage information<br>
Knowledge Shopping CPA data collection consent: check `Yes, I agree`<br>
Search Ad web log analysis use status: check `Use`

⑤ Confirm.

![WhoisMall_01]({{"/assets/img/whoismall_01.png"| relative_url}})

To use conversion types other than `purchase completion` (sign-up, add to cart, application/reservation, etc.), you must manually insert the script into skins or similar areas provided by the hosted mall. 
For manual script insertion, contact NHN Data, the official vendor for NAVER Ads conversion analysis scripts, and they will support installation and testing. Please contact the channels below.

 . Customer Center (phone): 1877-7035 <br>
 . Channel Talk (chat) consultation: [https://navercts.channel.io/home](https://navercts.channel.io/home) <br>
 . Public email: navercts@nhndata.com <br>

Ver: 240704_01
