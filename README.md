# React JS Landing Page Template
### <a href="https://open-science.vliz.be/example-bon-site-to-pages/" target="_blank">LIVE DEMO</a> 

#### The demo repo is located [here](https://github.com/vliz-be-opsci/example-bon-site-to-pages)

# Test if it is unique 

## Description
This is a ReactJS based landing page template.
All 'visual' data can be easily modified by changing the json files located in the data folder.

## Make it Yours!
### 1. Add your own data 
Change the data in the ```data/``` folder as well as add any images to ```img/``` folder.

#### 1.1. Data Structure

the data is stored in json files in the ```data/``` folder. This folder contains the following files:
*  [```main_data.json```](#211-main_datajson) -> contains the data for the header section
*  [```project_crates.json```](#212-project_cratesjson) -> contains the data for the project crates section
*  [```project_profiles.json```](#213-project_profilesjson) -> contains the data for the project profiles section
*  [```contacts.json```](#214-contactsjson) -> contains the data for describing the project contacts
*  [```tabular_data.json```](#215-tabulardatajson) -> contains the data for the tabular data page
*  [```publications.json```](#216-publicationsjson) -> contains the data for the publications section

there is also a ```README.md``` file that is used to populate the about section of the page. This file can be changed to your liking. For tips on how to write markdown files, see [here](https://guides.github.com/features/mastering-markdown/).

In the ```img/``` folder you can add any images that you want to use in the project. These images can be referenced in the json files.

##### 1.1.1. ```main_data.json```

This file contains the data for the header section. The structure of the file is as follows:
```json
{
    "name_site": "ARMS",
    "main_image": "https://assets.newatlas.com/dims4/default/e58452e/2147483647/strip/true/crop/1498x999+0+0/resize/1440x960!/quality/90/?url=http%3A%2F%2Fnewatlas-brightspot.s3.amazonaws.com%2Fb1%2Fb4%2F2a5bc31341fbaa31e2230d038f66%2Ficture1.jpeg",
    "description": "The European ARMS programme (ARMS-MBON) is a network of Autonomous Reef Monitoring Structures (ARMS) placed in the vicinity of marine stations, ports, marinas, and Long-Term Ecological Research (LTER) sites distributed over Europe and polar regions. The aim of ARMS-MBON is to assess the status of, and changes in, hard-bottom communities of near-coast environments, using genetic methods supplemented with image analysis and visual inspection methods. ARMS-MBON is part of GEO BONs Marine Biodiversity Observation Network (MBON).",
    "long_name": "Autonomous Reef Monitoring System",
    "short_name": "ARMS",
    "logo": "https://www.researchobject.org/ro-crate/assets/img/ro-crate-w-text.svg",
    "markdown_about_us":"README.md"
}
```

| Field | Description | required |
| --- | --- | --- |
| ```name_site``` | The name of the site | yes |
| ```main_image``` | The url to the main image of the site | no |
| ```description``` | The description of the site | yes |
| ```long_name``` | The long name of the site | yes |
| ```short_name``` | The short name of the site | yes |
| ```logo``` | The url to the logo of the site | no |
| ```markdown_about_us``` | The markdown file to be used for the about us page (default:README.md) | no |

##### 1.1.2. ```project_crates.json```

This file contains all the crates of the project.
```json
[
    {
    "icon": "fa fa-wordpress",
    "name": "Lorem ipsum dolor",
    "url" : "http://www.google.com",
    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis sed dapibus leo nec ornare diam sedasd commodo nibh ante facilisis bibendum dolor feugiat at."
  },
  {
    "icon": "fa fa-cart-arrow-down",
    "name": "Consectetur adipiscing",
    "url" : "http://www.google.com",
    "text": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis sed dapibus leo nec ornare diam sedasd commodo nibh ante facilisis bibendum dolor feugiat at."
  }
]
```

| Field | Description | required |
| --- | --- | --- |
| ```icon``` | The icon to be displayed | no |
| ```name``` | The name of the crate | yes |
| ```url``` | The url to the crate | yes |
| ```text``` | The description of the crate | no |


##### 1.1.3. ```project_profiles.json```

This file contains all the profiles for the project. These will most likely be links to your github repos.

```json
[
    {
      "icon": "fa fa-comments-o",
      "title": "Lorem ipsum",
      "url" : "http://www.google.com",
      "text": "Lorem ipsum dolor sit amet placerat facilisis felis mi in tempus eleifend pellentesque natoque etiam."
    },
    {
      "icon": "fa fa-bullhorn",
      "title": "Lorem ipsum",
      "url" : "http://www.google.com",
      "text": "Lorem ipsum dolor sit amet placerat facilisis felis mi in tempus eleifend pellentesque natoque etiam."
    }
]
```

| Field | Description | required |
| --- | --- | --- |
| ```icon``` | The icon to be displayed | no |
| ```title``` | The title of the profile | yes |
| ```url``` | The url to the profile | yes |
| ```text``` | The description of the profile | no |

##### 1.1.4. ```contacts.json```

This file contains all the contacts for the project. These will most likely be links to your github repos.

```json
[
    {
        "img": "img/contacts/01.jpg",
        "name": "Hugh Jass",
        "job": "Corporate Directives Executive",
        "email": "Hugh_Jasst@doe.com",
        "ORCID": "0000-0000-0000-0000",
        "affiliation": {
            "name": "University of Test",
            "id": "0000-0000-0000-0000",
            "url": "http://www.test.com"
        }
      },
      {
        "img": "img/contacts/02.jpg",
        "name": "Mike Hawk",
        "job": "Future Solutions Planner",
        "email": "hotmale@hotmail.com",
        "ORCID": "0000-0000-0000-0000",
        "affiliation": {
            "name": "University of Test",
            "id": "0000-0000-0000-0000",
            "url": "http://www.test.com"
        }
      }
]
```

###### 1.1.4.1 person

| Field | Description | required |
| --- | --- | --- |
| ```img``` | The image of the contact | no |
| ```name``` | The name of the contact | yes |
| ```job``` | The job of the contact | yes |
| ```email``` | The email of the contact | yes |
| ```ORCID``` | The ORCID of the contact | no |
| ```affiliation``` | The affiliation of the contact | no |


###### 1.1.4.2 affiliation

| Field | Description | required |
| --- | --- | --- |
| ```name``` | The name of the affiliation | yes |
| ```id``` | The id of the affiliation | no |
| ```url``` | The url of the affiliation | no |

##### 1.1.5. ```tabular_data.json``` WILL BE DEPRECATED

This file contains all the tabular data for the project. These will most likely be links to your github repos.

```json
[
    {
      "name": "combined imagedata",
      "url": "https://github.com/arms-mbon/Data/blob/main/QualityControlledData/Combined/combined_ImageData.csv",
      "description": "tabular data of all images in the combined dataset",
      "extra_info": "https://github.com/arms-mbon/Data/blob/main/QualityControlledData/Combined/README.md"
    },
    {
      "name": "test 2",
      "url": "https://github.com/arms-mbon/Data/blob/main/QualityControlledData/Combined/combined_ImageData.csv",
      "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nunc sit amet aliquam lacinia, nisl nisl aliquam nisl, nec aliquam nisl nisl"
    },
]
```

| Field | Description |
| --- | --- |
| ```name``` | The name of the tabular data |
| ```url``` | The url of the tabular data |
| ```description``` | The description of the tabular data |
| ```extra_info``` | The extra info of the tabular data (Optional)|

##### 1.1.6. ```publications.json```

This file contains all the publications information for the project. These will most likely be links to your publications uri's.

```json
[
    {
        "title": "Something Something interesting",
        "text": "Text about something interesting here A",
        "img": "/img/publications/1.jpg",
        "link": "https://www.youtube.com/watch?v=dQw4w9WgXcQ&ab_channel=RickAstley"
    },
    {
        "title": "The cat in the hat",
        "text": "The cat in the hat sat on the mat. One hopes he didn't leave a fat cat track in the form of a shattered mat.",
        "img": "/img/publications/2.jpeg",
        "link": "https://www.youtube.com/watch?v=dQw4w9WgXcQ&ab_channel=RickAstley"
    }
]
```

| Field | Description | required |
| --- | --- | --- |
| ```title``` | The title of the publication | yes |
| ```text``` | The text of the publication | yes |
| ```img``` | The image of the publication | preferably yes |
| ```link``` | The link to the publication | yes |

### 2. Deployment

the project is deployed using github pages. To deploy the project, simply push the changes to the master branch. The project will be deployed automatically.

#### 2.1. Resolving conflicts

##### 2.1.1. ```Action failed with "The process '/usr/bin/git' failed with exit code 128"```
Resolve this issue by following the steps below:
* Go to the settings of the repository
* Click on the actions tab and then the general button
* scroll down until you see the section "Workflow permissions"
* Select the option "Read and write permissions" and click save

## Credits
##### Free CSS 
<a href="https://www.free-css.com/assets/files/free-css-templates/preview/page234/interact/">Free-CSS.com </a>
