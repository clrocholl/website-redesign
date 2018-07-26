# Florida Energy Systems Consortium

## Website Redesign Proposal

Prepared for: UW HTML5 300 A

Author: Claudia Gomez-Rocholl

Date: July 16, 2018

URL: [http://floridaenergy.ufl.edu/](http://floridaenergy.ufl.edu/)

This is a proposal for the responsive redesign of the current Florida Energy Systems Consortium (FESC) website.


# Purpose

The FESC was created by the Florida State government to collaborate with Florida’s distinguished state universities to share energy-related expertise. The consortium also assists in the development of efficient forms of energy generation, consumption, and distribution. In order to share information and communicate with the public, the FESC created a website. 

Unfortunately, this website is difficult to use and navigate and does not comply with industry best practices for web design. The purpose of this redesign is to overhaul the FESC website to continue to attract readers and to ensure that it complies with best practices, accessibility standards, and mobile design principles.

# State of the Current Site

Before developing a redesign plan, I conducted a review to analyze and document the state of the current site in terms of performance, functionality, accessibility, ease of use, and mobile friendliness. 

## Accessibility Audit
Accessibility allows people with disabilities to perceive, understand, navigate, and interact with the web. For the accessibility review, I run the homepage through a web accessibility evaluation tool (https://wave.webaim.org/) to understand how well the website meets minimum WCAG 2.0 Guidelines. On that page only, the tool found nearly 22 errors and 7 alerts as shown in the following table:

**_Table 1_** _Accessibility Issues and Recommendations_


| Findings | Type | Ocurrences | Guideline | Recommendation |
| ------ | ------ | ------ | ------ | ------ |
| Linked image missing alternative text (Alt) | Perceivable error | 6 | Images that are the only thing within a link must have descriptive alternative text. If an image is within a link that contains no text and that image does not provide alternative text, a screen reader has no content to present to the user regarding the function of the link. | Add appropriate alternative text that presents the content of the image and/or the function of the link. |
| Image missing alternative text | Perceivable error | 3 | Provide text alternatives for any non-text content so that it can be changed into other forms people need, such as large print, braille, speech, symbols or simpler language. | Add an alt attribute to the image. The attribute value should accurately and succinctly present the content and function of the image. If the content of the image is conveyed in the context or surroundings of the image, or if the image does not convey content or have a function, it should be given empty/null alternative text (alt=""). |
| Missing form label | Perceivable error | 1 | If a form control does not have a properly associated text label, the function or purpose of that form control may not be presented to screen reader users. Form labels also provide visible descriptions and larger clickable targets for form controls. | If a text label for a form control is visible, use the <label> element to associate it with its respective form control. If there is no visible label, either provide an associated label, add a descriptive title attribute to the form control, or reference the label(s) using aria-labelledby. Labels are not required for image, submit, reset, button, or hidden form controls. |
| Empty heading | Operable error | 1 | Some users, especially keyboard and screen reader users, often navigate by heading elements. An empty heading will present no information and may introduce confusion. | Ensure that all headings contain informative content. |
| Contrast errors | Perceivable error | 11 | The visual presentation of text and images of text has a contrast ratio of at least 4.5:1. Large Text Large-scale text and images of large-scale text have a contrast ratio of at least 3:1. | This guideline helps users with low vision, color blindness, or worsening vision see and read the text on your screen. Use tools that can help you find an accessible color palette for your design. Take into consideration that placeholder or ghost text for form fields are not exempt from this standard. |
| Suspicious link text | Alert | 1 | Links, which are often read out of context, should clearly describe the destination or function of the link. Ambiguous text, text that does not make sense out of context, and extraneous text (such as "click here") can cause confusion and should be avoided. | Where appropriate, reword the link text so that it is more descriptive of its destination when read out of context. Remove any extraneous text (such as "click here"). |
| Redundant link | Alert | 4 | When adjacent links go to the same location (such as a linked product image and an adjacent linked product name that go to the same product page) this results in additional navigation and repetition for keyboard and screen reader users. | If possible, combine the redundant links into one link and remove any redundant text or alternative text (for example, if a product image and product name are in the same link, the image can usually be given alt=""). |
| Link to PDF document | Alert | 1 | Unless authored with accessibility in mind, PDF documents often have accessibility issues. Additionally, PDF documents are typically viewed using a separate application or plug-in, and can thus cause confusion and navigation difficulties. | Ensure the PDF document is natively accessible. Additionally, inform the user that the link will open a PDF document. Because PDF documents may have limitations in accessibility (particularly for complex content) and require a separate program, HTML content should often be used in place of or in addition to the PDF document. |
| Nonscript element | Alert | 1 | Content within <noscript> is presented if JavaScript is disabled. Because nearly all users (including users of screen readers and other assistive technologies) have JavaScript enabled, <noscript> cannot be used to provide an accessible version of inaccessible scripted content. | Ensure that scripted content is accessible. The <noscript> content will be presented to very few users, but must be accessible if used. |

## Mobile Friendliness
Ensuring that users with mobile devices can easily access and navigate the site is key when designing your website. I used Google Mobile-Friendly Test to test the mobile responsiveness of the FESC website. The test found that the FESC website is not mobile friendly. The improvements needed are shown in the following table:

**_Table 2_** _Mobile Friendliness Issues and Recommendations_

| Issue | Recommendation |
| ------ | ------ |
| Text too small to read | This report identifies pages where the font size for the page is too small to be legible and would require mobile visitors to “pinch to zoom” in order to read. After specifying a viewport for your web pages, set your font sizes to scale properly within the viewport. |
| Clickable elements too close together | Buttons and navigational links are so close to each other that a mobile user cannot easily tap a desired element with their finger without also tapping a neighboring element. To fix these errors, make sure to correctly size and space buttons and navigational links to be suitable for mobile visitors. |
| Content wider than screen | This report indicates pages where horizontal scrolling is necessary to see words and images on the page. This happens when pages use absolute values in CSS declarations, or use images designed to look best at a specific browser width (such as 980px). To fix this error, make sure the pages use relative width and position values for CSS elements, and make sure images can scale as well. |
| Viewport not set | Because visitors to your site use a variety of devices with varying screen sizes—from large desktop monitors, to tablets and small smartphones—your pages should specify a viewport using the meta viewport tag. This tag tells browsers how to adjust the page’s dimension and scaling to suit the device. |

## Performance
To analyze the FESC website performance, I used WebPageTest and PageSpeed Insights. Both tests showed that significant changes are needed to promote faster response times. The webpage took an average of 4 seconds to fully load (including images, scripts, and styling). 
Metric considerations according to MachMetrics Speed Blog:
* 53% of people leave a mobile page if it takes longer than 3 seconds do to load.
* The average page load speed for business and industry websites in the US in 2018 is 8.7 seconds.

The optimization suggestions for mobile and desktop devices are as follows:
* Eliminate render-blocking JavaScript and CSS in above-the-fold content
* Reduce server response time
* Leverage browser caching
* Optimize images
* Minify CSS
* Minify JavaScript

## Functionality
Functionality tests help verify whether the site meets the intended functional requirements. Different validations were performed to test the features and operational behavior of the website. The results are shown as follows:
### Manual Test Results

**_Table 3_** _Manual Functionality Test_

| Page | Result |
| ------ | ------ |
| Homepage | Clicking the Download Brochure link results in a 404 error. |
| Homepage | Clicking the LinkedIn icon enlarges the image, rather than taking you to LinkedIn. |
| Homepage | Clicking the sign up mail image opens the envelope image, rather than opening a mailto link. |

### Automated Tests Results

**_Table 4_**  _Automated Functionality Tests_

| Test | Result |
| ------ | ------ |
| HTML Validation | W3C Markup Validation Service reported 34 errors and 25 warnings while checking the FESC's homepage HTML. |
| CSS Validation | W3C CSS Validation Service reported 31 errors and 274 warnings while checking FESC’s CSS. |
| Linking Validation | [Broken Link Checker](http://www.brokenlinkcheck.com/) reported 307 broken links throughout the website. |

## Ease of Use
A website's ease of use is an integral part of its success as it determines if users can interact with it effectively. For this proposal, I evaluated the usability of the website by using a practical test offered by [usability.gov](https://www.usability.gov/), the emphasis is on pragmatic strategies that most site owners and users can do.

**_Table 5_**  _Usability Test_

| Usability Factor | Result |
| ------ | ------ |
| Intuitive design | The site’s design and information architecture are not intuitive, therefore information is difficult to find. The site’s navigation offers too many options to choose from. When I clicked the top navigation links to other landing pages, the navigation became more difficult as each new landing page displays a large side bar with numerous links. |
| Ease of learning | As a user who has never seen the user interface before, it took me at least 2 minutes to accomplish a basic task (decide where to go after I analyzed what information could be located under which menu). The site does not provide ease of learning and the navigation layout does not help. |
| Efficiency of use | Then, as a more experienced user of this page, I was not able to perform tasks optimally. There are ways to streamline and reduce the time it takes to complete a task, for instance, providing better labels and avoiding redundant information. |
| Memorability | After visiting the site quite a few times, I was not able to remember it enough to use it effectively. I was navigating back and forth pages to find the information I was looking for. |
| Error frequency and severity | While navigating and using the site, I did not find system errors other than the broken links reported in the Functionality section. |
| Subjective satisfaction | I did not find the design very attractive. In addition, it is not very easy to use as there are too many links and large units of text throughout the entire site. Information is not well presented making it very difficult to read. |

# Device Support
[Responsive Design Checker](http://responsivedesignchecker.com/) was used evaluate the device support of FESC’s website and to view the homepage in different client devices ranging from iPhones to large desktop monitors. The website does not support mobile devices smaller than the iPad Pro. Most of the content does not adapt and adjust to the display size of the client device. 
The following table lists the recommendations to improve the site’s device support:

**_Table 6_**  _Device Support Recommendations_

| Recommendation | Description |
| ------ | ------ |
| Set the viewport on the HTML | The viewport is the user's visible area of a web page. The viewport varies with the device, and is smaller on a mobile phone than on a computer screen. Include the <meta> viewport element in all the HTML pages (<meta name="viewport" content="width=device-width, initial-scale=1.0">). A <meta> viewport element gives the browser instructions on how to control the page's dimensions and scaling. The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device). The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser (W3schools.com). |
| Add breakpoints | Add a breakpoint where certain parts of the design will behave differently on each side of the breakpoint. Since there are multiple screens and devices with different heights and widths, you can target these five common groups: Extra small devices (phones, 600px and down), small devices (portrait tablets and large phones, 600px and up), medium devices (landscape tablets, 768px and up), large devices (laptops/desktops, 992px and up), extra-large devices (large laptops and desktops, 1200px and up). |

# Recommendations
At a high level, the following recommendations are provided for a responsive redesign of the FESC website:
* Keep users in mind and explore different Information Architecture (IA) strategies to improve the site maintenance and the metadata field description as well as to redesign the organization and labelling systems and also the navigation system.
* Address accessibility issues to meet WCAG 2.0 guidelines to ensure all users can perceive, understand, interact, and use the website.
* Fix performance issues to improve page load speed to meet mobile and industry average times and avoid user frustration.
* Address functionality issues and fix all broken links as well as HTML and CSS validation issues.
* Redesign the site’s page layouts to create modular elements that can increase ease of learning and use.
* Implement and set viewport, responsive layouts, and breakpoints to adjust content for mobile, tablet, and desktop devices.
