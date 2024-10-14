# Power-BI-Custom-Themes-and-Cohesive-Corporate-Branding

### Creating a Turnkey Corporate Brand for your Power BI Development Org

Before -> After Visualization

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

Under Report Theme JSON Schema we can download the latest version of the reportThemeSchema.JSON. 
![image](https://github.com/user-attachments/assets/bf260347-b27d-4e43-b099-be73e33e2e15)

For ease of access I recommend moving the schema file to the same folder as your to-be-created VS code file. If you plan on version controlling the report theme this should be in whatever GitHub linked folder you prefer. 

![image](https://github.com/user-attachments/assets/8000bada-6389-4235-981f-2d6d0c4bb93d)

Then you will want to create a new VS code JSON file by:
1. Opening VS code, and clicking open folder to path to and open the folder you saved the JSON Schema file in or cloning a repository if you are going to use version control. 
![image](https://github.com/user-attachments/assets/e2fc605e-6d03-4e4a-b93e-f53a9ec23241)

2. Selecting "New Text File"
![image](https://github.com/user-attachments/assets/d8f8deb8-bd73-4be7-97a1-870d936ec224)

3. Clicking "Select a language"

4. Type in and click ".JSON"
![image](https://github.com/user-attachments/assets/a01b51ff-f73c-46c9-90da-dad540e1ca81)



### Integrating Our Trader Joes Style Elements Into our JSON Theme File

### Transforming our Generic Dashboard Automatically with our Theme File







https://code.visualstudio.com/docs/languages/json#_json-schemas-and-settings

