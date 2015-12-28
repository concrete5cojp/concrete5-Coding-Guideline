# concrete5 Coding Guideline (5.7.x)

Switch branch for different language and versions.

- concrete5.7.3.1 and later
- Up to concrete5.7.5.3
- Updated on 2015/12/28
- Authored by Katz Ueno (concrete5 Japan, Inc.)
- GitHub: https://github.com/katzueno/concrete5-Coding-Guideline


<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>

Pull requests are welcome!
Please help fix any misspell, grammar error and others to improve!


## Translations

Language | URL
----|----
English | https://github.com/katzueno/concrete5-Coding-Guideline/tree/english
Japanese (日本語) | https://github.com/katzueno/concrete5-Coding-Guideline/tree/japanese


Additional translation are welcome! Please fork it, make a branch for the language, translate and send me the pull request!

**I'm still translating English.**


# About This Guideline

## Purpose

This guideline was made for front-end engineer who is creating an original concrete5 for client specific work.

concrete5 is front-end flexible CMS. But it also means that it be could easily resulted in CSS and/or JS conflict between site's CSS and interface UI..

This coding guideline is made to help avoid the conflict for concrete5 Japan, Inc. partners.

concrete5 Japan, Inc. is helping various company's concrete5 project. Please feel free to contact us at any time for your project needs. We can work internationally.

http://concrete5.co.jp/

## Target

This coding guildeline targets to the following:

- Have the knowledge of HTML + CSS + JS
- Have the basic knowledge of concrete5
- Building an original concrete5 theme based on the client's request
- Design is usually provided via Photoshop PSD, Illustrator's AI or other design data. And then crete HTML+CS+JS template

Additionally, we recommend the front-end engineer to closely get in touch with the designer during design process.

## License

This work is licensed under a Creative Commons Attribution 4.0 International License.

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a>

Use this guideline "as is". We hold no responsibility against any damages caused by this guideline.

By using this guideline, you have agreed that concrete5 Japan, Inc and its affiliate hold no responsibility or liability against any damages caused by using this guideline.

## Disclaimer

This guideline will always be work-in-progress.

There is no perfect way to code perfeclty.

Please use this guideline "as is". We hold no responsibility against any damages caused by this guideline.

## Credit

- Katz Ueno (concrete5 Japan, Inc) - http://concrete5.co.jp
- Remo Laubacher (Ortic Solutions GmbH) - http://www.ortic.com


# Example: Basic Specification

This is an example table for a project before you start coding.

## Example: Basics

Name | Content
----|----
Theme Handle | ***
Framework used | Bootstrap / Foundation / 960Grid / Original


## Example: Libraries Using

Please indicate which libraries you are planning to use

Libraries | Version
---- | ---
Bootstrap | 3.1.1
jQuery | 1.11.3
Bxslider | TBA


## Example: Page Template List

These page template handles are used for Body Wrapper Class in concrete5. So we recommend that you determine the following Page Template list before start coding.

Name | Handle
--- | ---
p0_0 Home | p0_0_top
p0_1 Department Top | p0_0_top_dept
p1_0 Default | default
p2_0 Product Top | p2_0_product_top
p2_1 Product Index | p2_1_product_index
p2_2 Product Detail | p2_1_product_detail

* You can only use letters, numbers and underscore (_)
* Underscore (_) will be converted to hyphen (-) when printed to the Body Wrapper Class **automatically**


## Example: Page Type List

These page type handles are used for Body Wrapper Class in concrete5. So we recommend that you determine the following Page Type list before start coding.

Name | Handle | Page Template used
--- | --- | ---
pt0_0 Home | pt0_0_top | p0_0_top
pt0_1_1 A Deaprtment Top | pt0_0_1_top_XX_dept | p0_0_top_dept
pt0_1_2 B Department Top | pt0_0_2_top_XX_dept | p0_0_top_dept
pt0_1_3 C Department Top | pt0_0_3_top_XX_dept | p0_0_top_dept
pt1_0_1 Default Index | default_index | default
pt1_0_2 Default Detail | default_page | default
pt2_0 Product Top | pt2_0_product_top | p2_0_product_top
pt2_1_1 Product Index Category A | pt2_1_1_product_index_XXX | p2_1_product_index
pt2_1_2 Product Index Category B | pt2_1_2_product_index_XXX | p2_1_product_index
pt2_1_3 Product Index Category C | pt2_1_3_product_index_XXX | p2_1_product_index
pt2_2_1 Product Detail Category A | pt2_1_1_product_index_XXX | p2_1_product_detail
pt2_2_2 Product Detail Category B | pt2_1_2_product_index_XXX | p2_1_product_detail
pt2_2_3 Product Detail Category C | pt2_1_3_product_index_XXX | p2_1_product_detail


* You can only use letters, numbers and underscore (_)
* Underscore (_) will be converted to hyphen (-) when printed to the Body Wrapper Class **automatically**


# Basic Rules

- You must use UTF-8 encoding
- You must use LF (UNIX) line break


# Where to Save

concrete5 saves the theme related files under the following locations.

Version | Destination
--- | ---
concrete5.6.x | /themes/XXX/
concrete5.7.x | /application/themes/XXX

* XXX should be replaced to your desired theme handle
* You can only use small letters, numbers and underscore (_). You CANNOT user CAPITAL letters.

The above locations are for your own theme. If you want to make your theme as 'package', You must follow it own rules. Please visit [concrete5 offocial documentatio section on concrete5.org](www.concrete5.org/documentation/developers/5.7/)


## Images, CSS and JS assets that are embedded onto theme

Images, CSS and JS assets should be saved onto the following locations. (These are files that are fixed onto the theme only.)

- /application/themes/XXX/css/
- /application/themes/XXX/js/
- /application/themes/XXX/images/

or

- /application/themes/XXX/assets/css/
- /application/themes/XXX/assets/js/
- /application/themes/XXX/assets/images/



## HTML Coding Location

We recommend you to save HTML mock ups under:

- /application/themes/XXX/html/

Please refer the same CSS, JS and images files that used for concrete5 themes files, so that it would be easier to debug.


# Library Set

Each cocnrete5 is shipped with the famous libraries.

If you plan to use the same libraries, you should try to use the same version of libraries to avoid conflict

**Especially, you should use same version of jQuery that concrete5 use**

Library Name |c5.6.3.3| c5.7.3.1 | c5.7.5.2 | c5.7.5.3
----- |---- | -----| -----|-----
ace | N/A | 1.1.8 | 1.2.0 | 1.2.2
backstretch | TBA | 2.0.4 | 2.0.4 | 2.0.4
bootstrap | 2.0.3 | 3.1.1 | 3.1.1 | 3.1.1
dropzone | N/A | 4.0.1 | 4.1.0 | 4.2.0
dynatree | N/A | 1.2.6 | 1.2.8 | 1.2.8
font-awesome | N/A  | TBA  | 4.2.0 | 4.2.0
html5shiv | N/A  | N/A | 3.7.2 | 3.7.2
respond | N/A  | N/A | 1.4.2 | 1.4.2
jquery | 1.7.2 | 1.11.1 | 1.11.3 | 1.11.3
jquery/awesome-rating | N/A | TBA  | 0.1.1 | 0.1.1
jquery/cookie |  N/A | 1.4.1 | 1.4.1 | 1.4.1
jquery/fileupload |  N/A | TBA | 5.39.0 | 5.39.0
jquery/form |  N/A | TBA | 2.87 | 2.87
jquery/live-update |  N/A | TBA | TBA | TBA
jquery/magnetic-pop-up |  N/A | TBA | TBA | 1.0.0
jquery/mousewheel |  N/A | TBA | TBA | 3.1.12
jquery/pep |  N/A | TBA | TBA | TBA
jquery/placeholder |  N/A | TBA | TBA | 2.0.8
jquery/tristate |  N/A | TBA | TBA | TBA
jquery/touch-punch | N/A | TBA | 0.2.3 | 0.2.3
jquery/ui | TBA | 1.10.3 | 1.11.4 | 1.11.4
jquery/visualize | N/A | TBA | TBA | TBA
kinetic | N/A | TBA | 4.7.2 | 4.7.2
Modernizr | N/A | TBA  | 2.8.3 | 2.8.3
packery | N/A | TBA | TBA | 1.0.2
picturefill | N/A | TBA | 2.3.1 | 2.3.1
redactor | N/A | TBA | 10.2.1 | 10.2.1
select2 | N/A | TBA | 3.5.1 | 3.5.1
spectrum | N/A | TBA | TBA | 1.3.4
swfobject | N/A | TBA | TBA | TBA
TinyMCE | 3.5.11 | N/A | N/A | N/A
underscore | N/A | TBA | 1.6.0 | 1.6.0

- N/A: not included in the core
- TBA: To be announced / currently checking its version.

If you want to specify how to load and unload these assets onto your theme, read the concrete5 documentation.

- [Requiring Core JavaScript or CSS in a Theme](http://documentation.concrete5.org/developers/designing-for-concrete5/advanced-css-and-javascript-usage/requiring-core-javascript-or-css-in-a-theme)
- [Overriding or Providing Core JavaScript or CSS in a Theme](http://documentation.concrete5.org/developers/designing-for-concrete5/advanced-css-and-javascript-usage/overriding-or-providing-core-javascript-or-css-in-a-theme)


# CSS/JS Framework

If you want to make a (responsive) concrete5 theme, concerte5 supports the following framework

- Bootstrap
- Foundation
- 960Grid

If you are not sure which framework to use, we recommend to use Bootsrap.

However, concrete5 use different version of Bootstrap. Be careful.

When using Foundation, you may need to be careful. But you don't get affected by the Bootstrap version.



# CSS Coding Guideline

## Do-nots & Cautions

### body Do-nots

#### Don't add ID and class to body (Required)

Don't add ID and class to body tag.

#### Don't apply Position to body (Required)

Don't add position to body.

#### No background (Recommended)

Don't add background to body. Please apply background to the following Body Wrapper Class


## don't use ccm-* classes (Required)

Except `ccm-page`, don't set any class naming `ccm-*` These are used for concrete5 UIs and dashboard.

## Body Wrapper Class (Required)

From concrete5.7.x, the div tag with following CSS classes are inserted right after the body tag; and it closes right before the end of body tag.

- ccm-page
- page-template-XXX (XXX is the handle of Page Templates)
- page-type-XXX (XXX is the handle of Page Type)

If you would like to apply certain overall design change depends on the Page Template and Types, you may use the above classes.

If you are not sure what to do, just ignore `page-template-XXX` and `page-type-XXX` classes but just ccm-page.


* To name Page Template and Page Type handles, you can use alphabet, number and underscore(_)
* However, underscore(_) will be **converted to hyphen (-) automatically** when printing it to the body wrapper class
* The user may leave the Page Type blank. Therefore, `page-type-xxx` may not be printed out to HTML sometime.


## Z-index (Required)

Z-index, for all of your CSS, must be set to less than 1000.

* In concrete5.6.x z-index must be set less than 5


## Don't do anything to depends on file upload location (Required)

Don't code anything that rely on uploading the images to the same directory where a concrete5 editor can freely edit and change.

- In concrete5, images and other assets are uploaded onto the directory which are randomly generated.
- For example, you won't be able to execute auto mouse over image effects by adding `_over` postfix to the file name. (unless the image assets are stored in theme folder and the image filename are hard-coded.)


## Don't add ID to blocks (Strongly Recommended)

Try to avoid any coding that uses ID.

## Meta title, description, keywords, OGP tag is not needed (Recommended)

Meta Tilte, Description, Keywords, OGP tags will be inserted. It's not necessary to implement for HTML coding.


# Coding Requirement

## Provide ALL patterns of blocks

- Based on the spec and design data, provide all design patterns of coding.
- Example: Left aliened, center, and right aliened image.

## Provide the patterns when the text, image and/or data is empty

- Consider the coding when elements are empty.
- Example: When thumbnail image of Page List is not present, the position, margin and padding of page title won't be messed up and etc.

## Consider the Pattern of Repeated Elements

- When showing the repeating elements, don't break the design layout by increasing and decreasing the number of elements.
- When showing the grid style elements, don't messed up the layout by increasing and decreasing the number of elements.
- When showing the grid style coding, don't wrap the elements by each row but entire section of the block.
- Make sure to provide coding with repeating elements of various patterns.
- If necessary, provide the coding when elements are empty or 1 entries when multiple entries are expected.
    - Example: When there is no result in Page List block, do you want to show other stuff or simply blank?
    - Example: When a slideshow block only has one image, do you still want to display pagination interface or transition effects?

## Consider the Size of Repeated Elements

- When coding grid content and must match the height of each elements, provide JavaScript to adjust the height of each element
- If JavaScript option is not available, consider to create a block that has one (1) row. And if you want to have multiple rows, add more blocks.
- Exmaple: There is a grid design Page List with thumbnail, date and page title elements. Whem the legth of page title differ, the height of each block differs and mess up the layout.


## Consider the Volume of Text

Consider the patterns when text is shorter and longer than expected.

- Example: When you have a aligned image + text block without proper clearfix, the layout could messed up when you have shorter text.
- Exmaple: There is a Page List block with thumbnail, date and title. If the page title become two-lines, it could messed up the layout.

## Consider Edit Bar on top when you have fixed navigation or anchor link

When a user with edit permission comes to concrete5 site, concrete5 will place 49px height edit bar on top. **This may cause some inconvenience to the editor.** She or he may not be able to see the global navigation or the anchor link will be right behind the edit bar.

Therefore, you may want to prepare the special CSS and JS code that will ONLY be inserted when the user see the edit bar.

SAMPLE

```
<?php $cp = new Permissions($c); if($cp->canViewToolbar()){?>
    <style media="screen">
        .header {top:48px;}
        /* Other CSS Style */
    </style>

    <script type="text/javascript">
        /* Additional setting such as smooth scrolling */
    </script>
    
<?php } ?>
```

# Coding Recommendation

## Try to make the block coding as generic as possible so that it can be used for other pages

- Blocks can be placed anywhere in the area (unless you resrtict via permission settings)
- Try to avoid the coding that can only be used at certain area. For example, the certain area is wrapped with certain div. The block is inheriting the CSS from it. (There may be some exception such as header, footer or the area with different background color)

## BEM (Block Elements Modifier)

We recommend to embrace BEM method.

https://en.bem.info/

## Use of LESS

From concrete5.7.x, it equipped with LESS compiler.
Except when previewing HTML template, there is no need to compile LESS.

We recommend to use LESS, But not necessary as long as you can provide compiled CSS file.


# Coding Guideline for Each Block

## Content

Content block uses Redactor JS library, and print out the following coding. It print out the code without class and ID. You may want to adjust your CSS by the following two patterns.

### Default

Content block won't wrap any div.

You may want to wrap the certain div in Area.

### Recommended

Make each Content block wrap with `<div class="wysiwyg"></div>`. In this case, you must override Content Block.

You should try to avoid the situation that a concrete5 user has to manually type CSS class or ID by going into code view of Content Block. If there is a certain pattern such as adding additional `<span>` tag to H tags, consider making a custom JS.


The following is the sample HTML coding of Content Block.

You should make CSS based on the following sample. Or we recommend to create the sample pattern by yourself by making a actual content block in concrete5, and provide those coding to the coder to adjust CSS>


```html
<div class="wysiwig"> <!-- This div tag is not generated via concrete5 default content block, but concrete5 Japan, Inc recommend this way. In order to achieve this, you must override Content Block. -->
    <p>P</p>

    <h1>H1</h1>

    <blockquote>
        Blockquote
    </blockquote>

    <p><strong>Strong</strong></p>

    <p><em>Italic</em></p>

    <p><u>Underscore</u></p>

    <p><del>Strikethrough</del></p>

    <p>UL&nbsp;List</p>

    <ul>
        <li>UL List</li>

        <li>UL List</li>

        <li>UL List</li>
    </ul>

    <p>OL List</p>

    <ol>
        <li>OL List</li>

        <li>OL List</li>

        <li>OL List</li>
    </ol>

    <p>No&nbsp;Indent</p>

    <p style="margin-left: 20px;">1 Indent</p>

    <p style="margin-left: 40px;">2 Indent</p>

    <p>Image</p>

    <p><img src="/index.php/download_file/view_inline/1"></p>

    <p>Align Left</p>

    <p>Align Right</p>

    <p>Table</p>

    <table>
        <thead>
            <tr>
                <td>Head</td>

                <td>Head</td>

                <td>Head</td>
            </tr>
        </thead>

        <tbody>
            <tr>
                <td>1</td>

                <td>2</td>

                <td>3</td>
            </tr>

            <tr>
                <td><p>Paragraph tag may get inserted upon certain situation</p>
                <p>When you happened to have the multiple lines text within a cell like this.</p></td>

                <td><p>Paragraph tag may get inserted upon certain situation</p>
                <p>When you happened to have the multiple lines text within a cell like this.</p></td>

                <td><p>Paragraph tag may get inserted upon certain situation</p>
                <p>When you happened to have the multiple lines text within a cell like this.</p></td>
            </tr>
        </tbody>
    </table>

    <p><a href="/index.php?cID=1" data-concrete5-link-type="ajax">Internal Link</a></p>

    <p><a href="/index.php/download_file/view/1" data-concrete5-link-type="image" data-concrete5-link-launch="lightbox-image">Light box Link - Image</a></p>

    <p><a href="/index.php?cID=1" data-concrete5-link-type="ajax" data-concrete5-link-launch="lightbox-image">Light box Link - AJAX</a></p>

    <p><a href="/index.php/download_file/view/1" data-concrete5-link-type="image">File Download Link</a></p>

    <p>Align Text to the Left</p>

    <p style="text-align: center;">Center text</p>

    <p style="text-align: right;">Align text to the right</p>

    <p style="text-align: justify;">Justify Text</p>
    <hr>

    <p><span style="color: rgb(192, 80, 77);">Font color</span></p>
</div>
<!-- This div tag is not generated via concrete5 default content block, but concrete5 Japan, Inc recommend this way. In order to achieve this, you must override Content Block. -->
```

## HTML Block

### Default

By default, HTML Block is wrapped with the following div

`<div id="HTMLBlockXXX" class="HTMLBlock">`

XXX is block ID.

### Recommended

Sometime, you don't want those HTMLBlock class or ID. Therefore, you may want to override HTML Block not to output div tag.


## Autonav

This is the navigation block based on list tag.

- You can add levels
- Commonly used for global navigation menu
- You could create mega menu via additioanl customization
- Breadcrumb is generated by this block

You could add additional div or span for each designated levels of navigation. However, it could be complicated. So please try to code with simple ul li structure.

## Page List

**Available elements**

- Page Title
- Published Date
- Thumbnail Imae
- Other Page Attributes
    - Topics
    - eyc

Wrap the entire block with div, and then create the repeatable elements


### Pagination

Although pagination has variety of options, it is recommended to code as the following.

#### Default Code of Pagination

Here is the sample code of pagination.

```html
<div class="ccm-pagination-wrapper">
    <ul class="pagination">
        <li class="prev"><a href="#">&larr; Previous</a></li>
        <li><a href="#">1</a></li>
        <li class="disabled"><span>&hellip;</span></li>
        <li><a href="#">17</a></li>
        <li><a href="#">18</a></li>
        <li><a href="#">19</a></li>
        <li><a href="#">20</a></li>
        <li><a href="#">21</a></li>
        <li><a href="#">22</a></li>
        <li class="active"><span>23 <span class="sr-only">(current)</span></span></li>
        <li class="next disabled"><span>Next &rarr;</span></li></ul></div>
```

The sample coding use Bootstrap 3.

###### 1. div wrapper

Please wrap with `<div class="ccm-pagination-wrapper">`

###### 2. ul

Please wrap with `<ul class="pagination">`.

###### 3. "Previous" Link


**FORMAT**

`<li class="prev"><a href="#">&larr; Previous</a></li>`

- Use `prev` class
- If there is no link, add `disable` class (If you don't want to display the previous link when it's not linked, please adjust CSS by using these classes.)
- Add `<span></span>`
- The text `&larr; Previous` can be configurable to any text

###### 4. Numbering: Basic

`<li><a href="#">7</a></li>`

- list tag
- a tag
- page number



###### 5. Numbering: Active Page

When displaying the page that you're currenltly viewing

`<li class="active"><span>23 <span class="sr-only">(current)</span></span></li>`

- active class added to the list tag
- wrap with span
- `<span class="sr-only">(current)</span>` is sample coding if you want to add additional coding for the current page. You could simply choose to leave ie blank.

###### 6. Numbering: Skip


`<li class="disabled"><span>&hellip;</span></li>`

- li tag with disabled class
- `<span>&hellip;</span>` to display '...'


###### 7. "Next"

`<li class="next disabled"><span>Next &rarr;</span></li></ul></div>`

- list tag
- with next class
- If there is no link, disabled class is added. (If you don't want to display the previous link when it's not linked, please adjust CSS by using these classes.)
- "Next &rarr;" is default text. But it can be configurable,

#### CSS File

In Page List block, it will load the
/concrete/css/frontend/pagination.css

But you sometime don't want to load extra css file.
You can either do any of the 2 steps

**1. Set page_theme.php to tell concrete5 that you're not using**

This is highly recommended option.

You are probably going to make new theme. So make sure to create page_theme.php and tell concrete5 that you won't be using any of frontend CSS files.


Example

```
<?php
public function registerAssets() {
    $this->providesAsset('css', 'core/frontend/pagination');
}
```

Then it won't load pagination CSS.


**2. Override /concrete/css/frontend/pagination.css**

Create a CSS file like /application/css/frontend/pagination.css
If you don't want anything, you can simply make a blank CSS file

**3. Override /concrete/blocks/page_list/controller.php**

Create a controller override of Page List block at /application/blocks/page_list/controller.php, then remove or comment the following line

`$this->requireAsset('css', 'core/frontend/pagination');` is.



#### Related Document of customizing Pagination

In addition, you can entirely customize the pagination format.

 - [Styling the pagination - 5.7](https://www.concrete5.org/documentation/how-tos/designers/styling-the-pagination-5.7/)


## Image Slider

**Available Elements**

- Image
- Title (Text)
- WYSIWYG (Similar to Content Block)
- Link

You can apply the similar coding to the page list block.
If you want to use any particular slideshow JS library, make sure it won't cause any conflict against concrete5's JS and other theme's JS.

If you want to create a image slideshow that has a thumbnail navigation, you must print out all thumbnail images in HTML, then use JS to create thumbnail navigation.
Example: http://memocarilog.info/memocarilog-demo/galleriffic-demo/

## Image Block

```html
<picture>
    <!--[if IE 9]><video style='display: none;'><![endif]--><!--[if IE 9]></video><![endif]-->
    <img src="/index.php/download_file/view_inline/1" alt="#" class="ccm-image-block img-responsive bID-XXXX">
</picture>
```

* 'bID-XXXX' will have its bID.


## FAQ Block

**Available Elements**

- Navigation Link Text
- Title Text
- Description

## Page Title

Working / help wanted

## Page Attribute

Working / help wanted

## YouTube

Working / help wanted

## Google Map

Working / help wanted

## Form Block

Working / help wanted
