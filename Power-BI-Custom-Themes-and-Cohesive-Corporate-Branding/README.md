# Power-BI-Custom-Themes-and-Cohesive-Corporate-Branding

### Creating a Turnkey Corporate Brand for your Power BI Development Org

![image](https://github.com/user-attachments/assets/1bf47370-fa95-4b7a-9eb7-374ffca8c9e1)

#### Should you create a Power BI Report Theme for your organization?

I don't recommend creating a branding theme if:
1. You are a small or one person data team with a limited portfolio of reports (less than 5) and don't have imminate plans for scaling reporting offerings as the time invested in creating a report theme for your organization will have limited value to the time investment.
2. You have no experience with coding outside of DAX/SQL as you may find the IDE enviroment of Visual Studio Code and simi-structured JSON data to be overwhelming.  

#### What Are the Benefits of Creating a Power BI Report Theme?

If you are a large or growing team with increasing report visibility and have some technical experience with Visual Studio Code or have experience with configuration files (XML, JSON, YAML) you probably already have, or should likely build one or multiple custom Power BI Report theme files for your organization. 

Some of the benefits of a custom report theme include:
1. Creating a structured and consistant visual style across multiple teams or BI developers
2. Reducing developer time spent on repeatedly fiddling with visuals and formatting
3. Enhancing visual interpretability, or contextual familiarity to enable quicker insight generation by data consumers.

A custom Power BI Report theme, along with an agile development framework and explicit, documented, user centered design best practices are leading indicators of a mature and value generating BI development team. 

### Identifying The Key Stylistic Elements of a Corporate Brand (Trader Joe's)

To create a custom branding theme for our Power BI reports, first we need to identify what the central branding identity elements are for an organization. Often, large organizations create and maintain documentation on their brand elements. This information is typically owned by the marketing team and could be called style guidelines, brand style guide, or something similar. 

This document should have information on brand colors and their meaning, including acceptable color combinations and motifs behind the color and other style choices that should inform your choices in the Power BI Theme JSON. For our example we will be inferring the style guidelines for a well known grocery store chain, Trader Joes. 

### Rengineering Style Guidelines for an Example Company (Trader Joe's)

Trader Joe's privately held medium to large grocery company known for carry unique and interesting products under its own store label. At TJ's staff wear hawaiian shirts, and the interior is reminiscent of a the inside of a ship. In my judgment, the company draws inspiration from nautical themes and an interpretation of the British East Indian Company that is perhaps rosier than it is historically accurate. 

#### Online Presence

![Trader_Joes_Brand_Colors](https://github.com/user-attachments/assets/b4be42de-2377-4efd-ba5d-df84f3d82c91)

Online, Trader Joe's website has a paper and ink feeling with use of beige colors, serif type, and styled visuals that feel hand drawn with layered color and pencil shading. They also make use of black border outlines and double horizontal lines to help frame their text boxes. 

In order to mimic this visual brand we should implement a Power BI Theme file that reproduces the following aspects:

1. White background 
2. Beige or tan foreground visuals
3. Seriffed font
4. Drop shadows
5. Black visual borders

By screenshotting and sampling visuals in MS Paint, or another product we are able to extract and create a list of hex codes that we will need for our Power BI theme. 

##### Primary TJ Colors
![image](https://github.com/user-attachments/assets/551adbac-8af2-4c9d-864f-64bae88b1817)

1. #C81E24 - Red, their primary brand and logo color
2. #2C2C2C - The black seen on their homepage
3. #FAFBF8 - The off white or beige on their homepage
4. #F1E99C - The yellow of the homepage bell
5. #093971 - A fun blue they use for their podcast page

To these primary brand colors we will add some important reporting specific colors such as:

1. #5f5f5f - A dark gray that will add some weight and utility to our power BI enviroment
2. #580C13 - A darker red to show value severity. Usually I would use a brighter red but that would be uncomfortable close to their primary brand color
3. #FFFFFF - The standard white seen on TJ's homepage and many others across the web
4. #D5A543 - A yellow that I like for neutral values
5. #3f9c6d - A green for postive values that feels in line with TJ's Brands use of tertiary colors

##### Secondary TJ Colors

![image](https://github.com/user-attachments/assets/a908333b-727b-4c3e-bb5f-7122e5e88c3d)


### Setting up a Power BI Report Theme file

#### What is a .JSON File?

JSON is a semi-structured file format that is both human readable and machine parsable. It is often used to pass and next semi-structured data within data engineering pipelines, and in this case, as a configuration file for Power BI. As far as configuration file formats go JSON is only somewhat annoying to read with XML being harder to read and YAML being easier to read. 

Due to the complexity of creating a Power BI Theme JSON from scratch. We will first download and link a schema file in a local directory that will allow us to better understand the required structure of the Report Theme file, and prompt us with syntax suggestions for each element as we format them. 

#### Using Visual Studio Code with a JSON Schema to Enable Intellisense 

The [Report Theme JSON Schema Repository](https://github.com/microsoft/powerbi-desktop-samples/tree/main/Report%20Theme%20JSON%20Schema) is available via Github and is referenced in the [official microsoft Power BI documentation](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-report-themes#set-visual-property-defaults-visualstyles) on desktop report themes.

Under Report Theme JSON Schema we can link the latest version of the hosted schema by clicking on the latest schema version on the left hand side of the page under "Report Theme JSON Schema", then clicking the raw button. You will want to save the hyperlink at the top of your browser at this point as you will need to paste it in a later step. 

**Navigating to the Schema**
![Navigating to the Schema](https://github.com/user-attachments/assets/45c5f23d-080e-41c8-8007-54c398f128a6)

**The Raw Schema Page and Hyperlink**
![RAW Schema Page Link](https://github.com/user-attachments/assets/10e78b2f-d767-4da0-b2fb-528edd51c72f)

**Then you will want to create a new VS code JSON file by:**

1. Opening VS code, and clicking open folder to path to or cloning a repository if you are going to use version control.

  ![image](https://github.com/user-attachments/assets/1d0ad8e0-7c51-4a04-b227-7db0cbd9b2b7)


2. Clicking file and Selecting "New Text File"
   
  ![image](https://github.com/user-attachments/assets/d8f8deb8-bd73-4be7-97a1-870d936ec224)

3. Clicking "Select a language" then type .JSON into the search bar and select the first option

![image](https://github.com/user-attachments/assets/a01b51ff-f73c-46c9-90da-dad540e1ca81)

4. Name your theme file and link the schema by using $schema using the below syntax along with the hyperlink you saved earlier

```
{"name":"Trader Joes Custom Power BI Theme",
"$schema": "https://raw.githubusercontent.com/microsoft/powerbi-desktop-samples/refs/heads/main/Report%20Theme%20JSON%20Schema/reportThemeSchema-2.136.json"

}
```
With the schema set up we can now start writing the syntax for each element we want for our Trader Joe's Report Theme while taking advantage of intelisense. 


### Integrating Our Trader Joes Style Elements Into our JSON Theme File

#### Data Colors

We will start by naming the hex codes for each data color in TJ's brand we identified earlier in our project. We will also call out good, neutral, and bad colors for use in conditional formatting. 

```
"dataColors":["#C81E24","#2C2C2C", "#FFFFFF", "#FAFBF8", "#F1E99C", "#093971", "#5f5f5f"],
"bad":"#580C13", 
"neutral":"#D5A543",
"good":"#3f9c6d",
```
This syntax when loaded as a theme will change our color palette from the Acessible Default:

![image](https://github.com/user-attachments/assets/a64d039e-a05a-42bf-8816-fc5fadc044fd)


To this:

![image](https://github.com/user-attachments/assets/345f631a-4be5-4297-b582-8eb5257d5647)


#### Seriffed Font

Next we will update our default fonts to a seriffed font that resembles the one that Trajer Joe's uses, Constantia. We will later need to use this font in our configirations for text boxes and visual headers. For all other text such as labels and values, we will use the default font Segoe UI. No one wants to look at table data in an unexpected or serrifed font after all. 


```
"textClasses": {
        "callout": {
            "fontSize": 45,
            "fontFace": "Constantia",
            "color": "#2C2C2C"
        },
        "title": {
            "fontSize": 14,
            "fontFace": "Constantia",
            "color": "#2C2C2C"
        },
        "header": {
            "fontSize": 12,
            "fontFace": "Constantia",
            "color": "#2C2C2C"
        },
        "label": {
            "fontSize": 10,
            "fontFace": "Segoe UI",
            "color": "#2C2C2C"
        }
```

#### White Background

Next we will change the outspace (the space behind the background) to beige and set our background to the default white by opening a nested option, visualStyles and setting options for various elements there.

```
"visualStyles":{
    "page":{
        "*":{
            "background":[{
                "color":{
                    "solid":{
                        "color":"#FFFFFF"}},
                "transparency":0}],
            "outspace":[{
                 "color":{
                     "solid":{
                         "color":"#FAFBF8"}}}]}}
}
```

#### Beige Foreground Visuals

We can set our configurations for multiple visual types at once within visual styles by using the asterisk "*"

```
"*":{
    "*":{
 
	    }
    }
```

To set all visual types to have beige foregrownd visuals we can write:

```
"*":{
    "*":{ 
    "background": [{"color":{"solid": {"color":"#FAFBF8"}}}]
	    }
    }
```

#### Drop Shadows

We can do the same for drop shadows on each of the visuals.

```
"dropShadow":   [{
                        "show": true,
                        "color": {"solid": {"color": "#5f5f5f"}},
                        "position":"Outer",
                        "preset":"BottomRight"}]
```

#### Black Visual Borders as Default Setting

```
"border":[
                    {"show": true},
                    {"color":{"solid": {"color":"#2C2C2C"}}}]
```

#### Modifying The Text Box Visual to Have Our Desired Background Color, Font, and Size Text with Black Boarders

As textbox isn't considered to be a graph or visual, we have to change its settings individually. 

```
 "textbox": {
        "*": {
            "*": [{
                "fontSize": 24,
                "fontFamily": "Constantia",
                "wordWrap": true,
                "fontColor": {"solid": {"color":"#2C2C2C"}},
                "background": { "solid": { "color": "#FAFBF8"}}}],
                
            "border":[
                    {"show": true},
                    {"color":{"solid": {"color":"#2C2C2C"}}}]    
                }},     
```


### Transforming our Generic Dashboard Automatically with our Theme File

Once we have constructed our JSON as outlined in the previous steps we can import it into our report by clicking "View", Selecting the dropdown, then clicking "Browse for Themes", and navigating via windows explorer to the JSON file. 

![image](https://github.com/user-attachments/assets/dccae4bb-612c-4a68-a5b7-82b2af973af1)





## The End Result of Our Theme File



![image](https://github.com/user-attachments/assets/81c1cf15-3342-43e1-8c1f-9d958bbf2947)
![image](https://github.com/user-attachments/assets/cdcb94b2-068d-4e17-a6cf-6f53f17781d9)


### Repeating Yourself

If you'd like to follow along with me, check out the following assets in the repo:
https://github.com/MattResner/Version-Controlled-Power-BI-Projects/blob/main/Power-BI-Custom-Themes-and-Cohesive-Corporate-Branding/TJ%20Power%20BI%20Theme.json
https://github.com/MattResner/Version-Controlled-Power-BI-Projects/blob/main/Power-BI-Custom-Themes-and-Cohesive-Corporate-Branding/Trader%20Joes%20Simulated%20Data.ipynb
https://github.com/MattResner/Version-Controlled-Power-BI-Projects/blob/main/Power-BI-Custom-Themes-and-Cohesive-Corporate-Branding/trader_joes_revenue_trending_simulation.csv

You may also clone the repo and open the report yourself, with the Trader Joe's Theme Active, and contribute by creating a branch and adding elements to the report. 
