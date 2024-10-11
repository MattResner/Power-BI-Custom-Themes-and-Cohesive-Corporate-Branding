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

Online, Trader Joe's website has a paper and ink feeling with use of beige colors, serif type, and styled visuals that feel hand drawn with layered colors and pencil shading. 

![Trader_Joes_Brand_Colors](https://github.com/user-attachments/assets/b4be42de-2377-4efd-ba5d-df84f3d82c91)


![image](https://github.com/user-attachments/assets/551adbac-8af2-4c9d-864f-64bae88b1817)


### Setting up a Power BI Branding JSON file.

#### What is a Json File?

#### Using Visual Studio Code with a JSON Schema to Enable Intelesense 






### Integrating Our Trader Joes Style Elements Into our JSON Theme File

### Transforming our Generic Dashboard Automatically with our Theme File


by visiting the homepage of trader joes we can see what sort of corporate identity they have and which colors they typically use. 

By pasting a screenshot of the page into ms paint we can extract the colors that are a major part of their identity. 

Trader joes uses the following

#C81E24 - Red, their primary branding color

#2C2C2C - The black seen on their homepage

#FFFFFF - the standard white seen on their homepage and many others

#FAFBF8 - The off white on their homepage

#F1E99C - The yellow of the homepage bell



#093971 - a fun blue they use for their podcast page. 

To these we will add some important other colors such:

#5f5f5f - a Dark gray that will add some weight and utility to our power BI enviroment

#580C13 - a darker red to show value severity. Usually I would use a brighter red but that would be uncomfortable close to their primary brand color

#D5A543 - an yellow that I like for neutral values

#3f9c6d - a green for postive values that feels in line with TJ's Brands use of teriarty colors




https://code.visualstudio.com/docs/languages/json#_json-schemas-and-settings

