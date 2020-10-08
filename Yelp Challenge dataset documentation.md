       

*   [Table of Contents](#contents)
*   [1\. Model](#model)
*   [2\. Databases](#containers)
    *   [2.1 yelp](#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6)
        
        [2.1.2. Collections](#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6)
        
        [2.1.2.1 businesses](#0dd7ead0-2b24-11e6-b7e5-591297143e36)
        
        [2.1.2.2 checkins](#a080d1d0-91f6-11e9-a924-ddc9cd9b071f)
        
        [2.1.2.3 reviews](#0da2aa00-2b24-11e6-b7e5-591297143e36)
        
        [2.1.2.4 tips](#0de02830-2b24-11e6-b7e5-591297143e36)
        
        [2.1.2.5 users](#0df0f110-2b24-11e6-b7e5-591297143e36)
        
*   [3\. Views](#views)
    *   [3.1 rov\_bussiness](#5c771580-5193-11e7-b9f2-49270a53df2c)
    *   [3.2 rov\_rev\_users](#090874c0-5206-11e7-8e65-9b1d6a151b1d)
*   [4\. Relationships](#relationships)
    *   [4.1 fk businesses.business\_id to checkins.business\_id](#003231f0-91f7-11e9-a924-ddc9cd9b071f)
    *   [4.2 fk\_reviewsBusinesses](#fb857d40-2b26-11e6-b7e5-591297143e36)
    *   [4.3 fk\_reviewsUsers](#e2514f70-2b26-11e6-b7e5-591297143e36)
    *   [4.4 fk\_tipsBusinesses](#8a3660f0-2b26-11e6-b7e5-591297143e36)
    *   [4.5 fk\_tipsUsers](#aa956d50-2b26-11e6-b7e5-591297143e36)

### <a id="documentation-body"></a>

![Hackolade image](/YelpChallengedatasetdocumentation_images/image1.png?raw=true)

MongoDB Physical Model
----------------------

#### Schema for:

Model name: Yelp Challenge dataset

Author: Pascal

Version: 1.2

File name: Yelp Challenge dataset.json

### <a id="file-path"></a>File path: C:\\Users\\Pascal\\Documents\\Hackolade\\Models\\MongoDB\\Yelp Challenge dataset.json### <a id="printed-on"></a>Printed On: Thu Oct 08 2020 19:44:36 GMT+0200 (Central European Summer Time)

Created with: [Hackolade](https://hackolade.com/) - Visual data modeling for NoSQL and multimodel databases

### <a id="contents"></a>

##### 1\. Model

##### 2\. Databases

*   [2.1 yelp](#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6)
    
    [2.1.2. Collections](#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6)
    
    [2.1.2.1 businesses](#0dd7ead0-2b24-11e6-b7e5-591297143e36)
    
    [2.1.2.2 checkins](#a080d1d0-91f6-11e9-a924-ddc9cd9b071f)
    
    [2.1.2.3 reviews](#0da2aa00-2b24-11e6-b7e5-591297143e36)
    
    [2.1.2.4 tips](#0de02830-2b24-11e6-b7e5-591297143e36)
    
    [2.1.2.5 users](#0df0f110-2b24-11e6-b7e5-591297143e36)
    

##### 3\. Views

*   [3.1 rov\_bussiness](#5c771580-5193-11e7-b9f2-49270a53df2c)
*   [3.2 rov\_rev\_users](#090874c0-5206-11e7-8e65-9b1d6a151b1d)

##### 4\. Relationships

*   [4.1 fk businesses.business\_id to checkins.business\_id](#003231f0-91f7-11e9-a924-ddc9cd9b071f)
*   [4.2 fk\_reviewsBusinesses](#fb857d40-2b26-11e6-b7e5-591297143e36)
*   [4.3 fk\_reviewsUsers](#e2514f70-2b26-11e6-b7e5-591297143e36)
*   [4.4 fk\_tipsBusinesses](#8a3660f0-2b26-11e6-b7e5-591297143e36)
*   [4.5 fk\_tipsUsers](#aa956d50-2b26-11e6-b7e5-591297143e36)

##### 1\. Model

##### 1.1 Model **Yelp Challenge dataset**

##### 1.1.1 **Yelp Challenge dataset** Entity Relationship Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image2.png?raw=true)

##### 1.1.2 **Yelp Challenge dataset** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td><span>Model name</span></td><td>Yelp Challenge dataset</td></tr><tr><td><span>Technical name</span></td><td>yelpChallengeDataset</td></tr><tr><td><span>Description</span></td><td><div class="docs-markdown"><p>Schema inferred from the reverse-engineering of a Yelp Challenge dataset available from <a href="https://www.yelp.com/dataset_challenge/dataset">https://www.yelp.com/dataset_challenge/dataset</a></p></div></td></tr><tr><td><span>Author</span></td><td>Pascal</td></tr><tr><td><span>Version</span></td><td>1.2</td></tr><tr><td><span>DB vendor</span></td><td>MongoDB</td></tr><tr><td><span>DB version</span></td><td>v4.2</td></tr><tr><td><span>Comments</span></td><td><div class="docs-markdown"><p>The dataset was downloaded and loaded to a MongoDB, then reverse-engineered with Hackolade. The relationships were manually documented to enrich the model.</p><p>This schema shows the power of JSON with the embedding of many attributes logically grouped, one form of implicit relationships. At the same time, the schema is fairly relational, which makes total sense given the conceptual entities. As a result, there's no denormalization. Given the size of the collections, it makes sense to perform this kind of traditional foreing key relationships.</p><p>Note that only fields found in 100% of the sampled documents are 'required' (and differentiated thanks to a solid line box) as opposed to the other fields with dashed line boxes.</p><p>The sampling parameters were:</p><ul><li>absolute up to 1000 documents max per collection</li><li>alpha order of fields</li></ul></div></td></tr></tbody></table>

##### 1.1.3 **Yelp Challenge dataset** DB Definitions

### <a id="0dd81200-2b24-11e6-b7e5-591297143e36"></a>1.1.3.1 Field **full\_address**

##### 1.1.3.1.1 **full\_address** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image3.png?raw=true)

##### 1.1.3.1.2 **full\_address** Hierarchy

Parent field: **Definitions**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#7107ebf0-dc5b-11e9-b819-e3f2d5171928>houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#760da090-dc5b-11e9-b819-e3f2d5171928>street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7bfbe070-dc5b-11e9-b819-e3f2d5171928>box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7ee803e0-dc5b-11e9-b819-e3f2d5171928>city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#85787730-dc5b-11e9-b819-e3f2d5171928>state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#87afc990-dc5b-11e9-b819-e3f2d5171928>zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 1.1.3.1.3 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Technical name</td><td>full_address</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="7107ebf0-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.2 Field **houseNum**

##### 1.1.3.2.1 **houseNum** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>houseNum</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>123</td></tr></tbody></table>

### <a id="760da090-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.3 Field **street**

##### 1.1.3.3.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>Main Street</td></tr></tbody></table>

### <a id="7bfbe070-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.4 Field **box**

##### 1.1.3.4.1 **box** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>box</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="7ee803e0-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.5 Field **city**

##### 1.1.3.5.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>Anytown</td></tr></tbody></table>

### <a id="85787730-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.6 Field **state**

##### 1.1.3.6.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>CA</td></tr></tbody></table>

### <a id="87afc990-dc5b-11e9-b819-e3f2d5171928"></a>1.1.3.7 Field **zip**

##### 1.1.3.7.1 **zip** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>zip</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>12345</td></tr></tbody></table>

### <a id="containers"></a>

##### 2\. Databases

### <a id="3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6"></a>2.1 Database **yelp**

##### 2.1.1 **yelp** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Database name</td><td>yelp</td></tr><tr><td>Technical name</td><td>yelp</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Enable sharding</td><td>true</td></tr><tr><td>Description</td><td><div class="docs-markdown"></div></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Custom container property</td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2 **yelp** Collections

### <a id="0dd7ead0-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1 Collection **businesses**

##### 2.1.2.1.1 **businesses** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image4.png?raw=true)

##### 2.1.2.1.2 **businesses** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>businesses</td></tr><tr><td>Technical name</td><td>businesses</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Id</td><td></td></tr><tr><td>Description</td><td><div class="docs-markdown"></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6>yelp</a></td></tr><tr><td>Capped</td><td></td></tr><tr><td>Size</td><td></td></tr><tr><td>Max</td><td></td></tr><tr><td>Storage engine</td><td></td></tr><tr><td>Validation level</td><td></td></tr><tr><td>Validation action</td><td></td></tr><tr><td>Additional properties</td><td></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Custom property</td><td></td></tr></tbody></table>

##### 2.1.2.1.3 **businesses** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr><tr><td><a href=#0dd81219-2b24-11e6-b7e5-591297143e36>name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#42970fb0-de10-11e9-b618-a12fa8f5b98e>full\_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7107ebf0-dc5b-11e9-b819-e3f2d5171928>houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#760da090-dc5b-11e9-b819-e3f2d5171928>street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7bfbe070-dc5b-11e9-b819-e3f2d5171928>box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7ee803e0-dc5b-11e9-b819-e3f2d5171928>city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#85787730-dc5b-11e9-b819-e3f2d5171928>state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#87afc990-dc5b-11e9-b819-e3f2d5171928>zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ff-2b24-11e6-b7e5-591297143e36>city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121f-2b24-11e6-b7e5-591297143e36>state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead2-2b24-11e6-b7e5-591297143e36>attributes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead3-2b24-11e6-b7e5-591297143e36>acceptsCreditCards</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead4-2b24-11e6-b7e5-591297143e36>acceptsInsurance</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead5-2b24-11e6-b7e5-591297143e36>alcohol</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead6-2b24-11e6-b7e5-591297143e36>ambience</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead7-2b24-11e6-b7e5-591297143e36>casual</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead8-2b24-11e6-b7e5-591297143e36>classy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead9-2b24-11e6-b7e5-591297143e36>divey</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eada-2b24-11e6-b7e5-591297143e36>hipster</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadb-2b24-11e6-b7e5-591297143e36>intimate</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadc-2b24-11e6-b7e5-591297143e36>romantic</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadd-2b24-11e6-b7e5-591297143e36>touristy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eade-2b24-11e6-b7e5-591297143e36>trendy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadf-2b24-11e6-b7e5-591297143e36>upscale</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae0-2b24-11e6-b7e5-591297143e36>attire</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae1-2b24-11e6-b7e5-591297143e36>byAppointmentOnly</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae2-2b24-11e6-b7e5-591297143e36>byob/corkage</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae3-2b24-11e6-b7e5-591297143e36>caters</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae4-2b24-11e6-b7e5-591297143e36>coatCheck</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae5-2b24-11e6-b7e5-591297143e36>delivery</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae6-2b24-11e6-b7e5-591297143e36>dogsAllowed</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae7-2b24-11e6-b7e5-591297143e36>drive-thru</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae8-2b24-11e6-b7e5-591297143e36>goodFor</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae9-2b24-11e6-b7e5-591297143e36>breakfast</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaea-2b24-11e6-b7e5-591297143e36>brunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaeb-2b24-11e6-b7e5-591297143e36>dessert</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaec-2b24-11e6-b7e5-591297143e36>dinner</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaed-2b24-11e6-b7e5-591297143e36>latenight</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaee-2b24-11e6-b7e5-591297143e36>lunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaef-2b24-11e6-b7e5-591297143e36>goodForDancing</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e0-2b24-11e6-b7e5-591297143e36>goodForGroups</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e1-2b24-11e6-b7e5-591297143e36>goodForKids</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e2-2b24-11e6-b7e5-591297143e36>happyHour</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e3-2b24-11e6-b7e5-591297143e36>hasTv</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e4-2b24-11e6-b7e5-591297143e36>music</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e5-2b24-11e6-b7e5-591297143e36>background\_music</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e6-2b24-11e6-b7e5-591297143e36>dj</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e7-2b24-11e6-b7e5-591297143e36>jukebox</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e8-2b24-11e6-b7e5-591297143e36>karaoke</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e9-2b24-11e6-b7e5-591297143e36>live</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ea-2b24-11e6-b7e5-591297143e36>video</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811eb-2b24-11e6-b7e5-591297143e36>noiseLevel</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ec-2b24-11e6-b7e5-591297143e36>open24Hours</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ed-2b24-11e6-b7e5-591297143e36>orderAtCounter</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ee-2b24-11e6-b7e5-591297143e36>outdoorSeating</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ef-2b24-11e6-b7e5-591297143e36>parking</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f0-2b24-11e6-b7e5-591297143e36>garage</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f1-2b24-11e6-b7e5-591297143e36>lot</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f2-2b24-11e6-b7e5-591297143e36>street</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f3-2b24-11e6-b7e5-591297143e36>valet</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f4-2b24-11e6-b7e5-591297143e36>validated</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f5-2b24-11e6-b7e5-591297143e36>priceRange</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f6-2b24-11e6-b7e5-591297143e36>smoking</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f7-2b24-11e6-b7e5-591297143e36>take-out</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f8-2b24-11e6-b7e5-591297143e36>takesReservations</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f9-2b24-11e6-b7e5-591297143e36>waiterService</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fa-2b24-11e6-b7e5-591297143e36>wheelchairAccessible</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fb-2b24-11e6-b7e5-591297143e36>wi-fi</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fd-2b24-11e6-b7e5-591297143e36>categories</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fe-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81201-2b24-11e6-b7e5-591297143e36>hours</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81202-2b24-11e6-b7e5-591297143e36>friday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81203-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81204-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81205-2b24-11e6-b7e5-591297143e36>monday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81206-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81207-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81208-2b24-11e6-b7e5-591297143e36>saturday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81209-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120a-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120b-2b24-11e6-b7e5-591297143e36>sunday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120c-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120d-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120e-2b24-11e6-b7e5-591297143e36>thursday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120f-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81210-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81211-2b24-11e6-b7e5-591297143e36>tuesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81212-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81213-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81214-2b24-11e6-b7e5-591297143e36>wednesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81215-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81216-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81217-2b24-11e6-b7e5-591297143e36>latitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81218-2b24-11e6-b7e5-591297143e36>longitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121a-2b24-11e6-b7e5-591297143e36>neighborhoods</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121b-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121c-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121d-2b24-11e6-b7e5-591297143e36>review\_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8121e-2b24-11e6-b7e5-591297143e36>stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81220-2b24-11e6-b7e5-591297143e36>type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0dd811fc-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.1 Field **business\_id**

##### 2.1.2.1.3.1.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr><tr><td>Comments</td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr></tbody></table>

### <a id="0dd81219-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.2 Field **name**

##### 2.1.2.1.3.2.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="42970fb0-de10-11e9-b618-a12fa8f5b98e"></a>2.1.2.1.3.3 Field **full\_address**

##### 2.1.2.1.3.3.1 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Technical name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>$ref</td><td>#model/definitions/full_address</td></tr><tr><td>Reference type</td><td>model</td></tr></tbody></table>

### <a id="0dd811ff-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.4 Field **city**

##### 2.1.2.1.3.4.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Technical name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121f-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.5 Field **state**

##### 2.1.2.1.3.5.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Technical name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead2-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.6 Field **attributes**

##### 2.1.2.1.3.6.1 **attributes** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image5.png?raw=true)

##### 2.1.2.1.3.6.2 **attributes** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7ead3-2b24-11e6-b7e5-591297143e36>Accepts Credit Cards</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead4-2b24-11e6-b7e5-591297143e36>Accepts Insurance</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead5-2b24-11e6-b7e5-591297143e36>Alcohol</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead6-2b24-11e6-b7e5-591297143e36>Ambience</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae0-2b24-11e6-b7e5-591297143e36>Attire</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae1-2b24-11e6-b7e5-591297143e36>By Appointment Only</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae2-2b24-11e6-b7e5-591297143e36>BYOB/Corkage</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae3-2b24-11e6-b7e5-591297143e36>Caters</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae4-2b24-11e6-b7e5-591297143e36>Coat Check</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae5-2b24-11e6-b7e5-591297143e36>Delivery</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae6-2b24-11e6-b7e5-591297143e36>Dogs Allowed</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae7-2b24-11e6-b7e5-591297143e36>Drive-Thru</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eae8-2b24-11e6-b7e5-591297143e36>Good For</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaef-2b24-11e6-b7e5-591297143e36>Good For Dancing</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e0-2b24-11e6-b7e5-591297143e36>Good For Groups</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e1-2b24-11e6-b7e5-591297143e36>Good for Kids</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e2-2b24-11e6-b7e5-591297143e36>Happy Hour</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e3-2b24-11e6-b7e5-591297143e36>Has TV</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e4-2b24-11e6-b7e5-591297143e36>Music</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811eb-2b24-11e6-b7e5-591297143e36>Noise Level</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ec-2b24-11e6-b7e5-591297143e36>Open 24 Hours</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ed-2b24-11e6-b7e5-591297143e36>Order at Counter</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ee-2b24-11e6-b7e5-591297143e36>Outdoor Seating</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ef-2b24-11e6-b7e5-591297143e36>Parking</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f5-2b24-11e6-b7e5-591297143e36>Price Range</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f6-2b24-11e6-b7e5-591297143e36>Smoking</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f7-2b24-11e6-b7e5-591297143e36>Take-out</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f8-2b24-11e6-b7e5-591297143e36>Takes Reservations</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f9-2b24-11e6-b7e5-591297143e36>Waiter Service</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fa-2b24-11e6-b7e5-591297143e36>Wheelchair Accessible</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811fb-2b24-11e6-b7e5-591297143e36>Wi-Fi</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.6.3 **attributes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>attributes</td></tr><tr><td>Technical name</td><td>attributes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead3-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.7 Field **Accepts Credit Cards**

##### 2.1.2.1.3.7.1 **Accepts Credit Cards** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Accepts Credit Cards</td></tr><tr><td>Technical name</td><td>acceptsCreditCards</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead4-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.8 Field **Accepts Insurance**

##### 2.1.2.1.3.8.1 **Accepts Insurance** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Accepts Insurance</td></tr><tr><td>Technical name</td><td>acceptsInsurance</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead5-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.9 Field **Alcohol**

##### 2.1.2.1.3.9.1 **Alcohol** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Alcohol</td></tr><tr><td>Technical name</td><td>alcohol</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead6-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.10 Field **Ambience**

##### 2.1.2.1.3.10.1 **Ambience** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image6.png?raw=true)

##### 2.1.2.1.3.10.2 **Ambience** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7ead7-2b24-11e6-b7e5-591297143e36>casual</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead8-2b24-11e6-b7e5-591297143e36>classy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7ead9-2b24-11e6-b7e5-591297143e36>divey</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eada-2b24-11e6-b7e5-591297143e36>hipster</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadb-2b24-11e6-b7e5-591297143e36>intimate</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadc-2b24-11e6-b7e5-591297143e36>romantic</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadd-2b24-11e6-b7e5-591297143e36>touristy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eade-2b24-11e6-b7e5-591297143e36>trendy</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eadf-2b24-11e6-b7e5-591297143e36>upscale</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.10.3 **Ambience** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Ambience</td></tr><tr><td>Technical name</td><td>ambience</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead7-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.11 Field **casual**

##### 2.1.2.1.3.11.1 **casual** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>casual</td></tr><tr><td>Technical name</td><td>casual</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead8-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.12 Field **classy**

##### 2.1.2.1.3.12.1 **classy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>classy</td></tr><tr><td>Technical name</td><td>classy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7ead9-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.13 Field **divey**

##### 2.1.2.1.3.13.1 **divey** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>divey</td></tr><tr><td>Technical name</td><td>divey</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eada-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.14 Field **hipster**

##### 2.1.2.1.3.14.1 **hipster** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hipster</td></tr><tr><td>Technical name</td><td>hipster</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadb-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.15 Field **intimate**

##### 2.1.2.1.3.15.1 **intimate** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>intimate</td></tr><tr><td>Technical name</td><td>intimate</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadc-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.16 Field **romantic**

##### 2.1.2.1.3.16.1 **romantic** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>romantic</td></tr><tr><td>Technical name</td><td>romantic</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadd-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.17 Field **touristy**

##### 2.1.2.1.3.17.1 **touristy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>touristy</td></tr><tr><td>Technical name</td><td>touristy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eade-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.18 Field **trendy**

##### 2.1.2.1.3.18.1 **trendy** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>trendy</td></tr><tr><td>Technical name</td><td>trendy</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eadf-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.19 Field **upscale**

##### 2.1.2.1.3.19.1 **upscale** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>upscale</td></tr><tr><td>Technical name</td><td>upscale</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae0-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.20 Field **Attire**

##### 2.1.2.1.3.20.1 **Attire** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Attire</td></tr><tr><td>Technical name</td><td>attire</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae1-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.21 Field **By Appointment Only**

##### 2.1.2.1.3.21.1 **By Appointment Only** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>By Appointment Only</td></tr><tr><td>Technical name</td><td>byAppointmentOnly</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae2-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.22 Field **BYOB/Corkage**

##### 2.1.2.1.3.22.1 **BYOB/Corkage** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>BYOB/Corkage</td></tr><tr><td>Technical name</td><td>byob/corkage</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae3-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.23 Field **Caters**

##### 2.1.2.1.3.23.1 **Caters** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Caters</td></tr><tr><td>Technical name</td><td>caters</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae4-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.24 Field **Coat Check**

##### 2.1.2.1.3.24.1 **Coat Check** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Coat Check</td></tr><tr><td>Technical name</td><td>coatCheck</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae5-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.25 Field **Delivery**

##### 2.1.2.1.3.25.1 **Delivery** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Delivery</td></tr><tr><td>Technical name</td><td>delivery</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae6-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.26 Field **Dogs Allowed**

##### 2.1.2.1.3.26.1 **Dogs Allowed** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Dogs Allowed</td></tr><tr><td>Technical name</td><td>dogsAllowed</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae7-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.27 Field **Drive-Thru**

##### 2.1.2.1.3.27.1 **Drive-Thru** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Drive-Thru</td></tr><tr><td>Technical name</td><td>drive-thru</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae8-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.28 Field **Good For**

##### 2.1.2.1.3.28.1 **Good For** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image7.png?raw=true)

##### 2.1.2.1.3.28.2 **Good For** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd7eae9-2b24-11e6-b7e5-591297143e36>breakfast</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaea-2b24-11e6-b7e5-591297143e36>brunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaeb-2b24-11e6-b7e5-591297143e36>dessert</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaec-2b24-11e6-b7e5-591297143e36>dinner</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaed-2b24-11e6-b7e5-591297143e36>latenight</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd7eaee-2b24-11e6-b7e5-591297143e36>lunch</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.28.3 **Good For** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For</td></tr><tr><td>Technical name</td><td>goodFor</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eae9-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.29 Field **breakfast**

##### 2.1.2.1.3.29.1 **breakfast** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>breakfast</td></tr><tr><td>Technical name</td><td>breakfast</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaea-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.30 Field **brunch**

##### 2.1.2.1.3.30.1 **brunch** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>brunch</td></tr><tr><td>Technical name</td><td>brunch</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaeb-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.31 Field **dessert**

##### 2.1.2.1.3.31.1 **dessert** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dessert</td></tr><tr><td>Technical name</td><td>dessert</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaec-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.32 Field **dinner**

##### 2.1.2.1.3.32.1 **dinner** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dinner</td></tr><tr><td>Technical name</td><td>dinner</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaed-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.33 Field **latenight**

##### 2.1.2.1.3.33.1 **latenight** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latenight</td></tr><tr><td>Technical name</td><td>latenight</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaee-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.34 Field **lunch**

##### 2.1.2.1.3.34.1 **lunch** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>lunch</td></tr><tr><td>Technical name</td><td>lunch</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd7eaef-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.35 Field **Good For Dancing**

##### 2.1.2.1.3.35.1 **Good For Dancing** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For Dancing</td></tr><tr><td>Technical name</td><td>goodForDancing</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e0-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.36 Field **Good For Groups**

##### 2.1.2.1.3.36.1 **Good For Groups** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good For Groups</td></tr><tr><td>Technical name</td><td>goodForGroups</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e1-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.37 Field **Good for Kids**

##### 2.1.2.1.3.37.1 **Good for Kids** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Good for Kids</td></tr><tr><td>Technical name</td><td>goodForKids</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e2-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.38 Field **Happy Hour**

##### 2.1.2.1.3.38.1 **Happy Hour** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Happy Hour</td></tr><tr><td>Technical name</td><td>happyHour</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e3-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.39 Field **Has TV**

##### 2.1.2.1.3.39.1 **Has TV** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Has TV</td></tr><tr><td>Technical name</td><td>hasTv</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e4-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.40 Field **Music**

##### 2.1.2.1.3.40.1 **Music** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image8.png?raw=true)

##### 2.1.2.1.3.40.2 **Music** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811e5-2b24-11e6-b7e5-591297143e36>background\_music</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e6-2b24-11e6-b7e5-591297143e36>dj</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e7-2b24-11e6-b7e5-591297143e36>jukebox</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e8-2b24-11e6-b7e5-591297143e36>karaoke</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811e9-2b24-11e6-b7e5-591297143e36>live</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811ea-2b24-11e6-b7e5-591297143e36>video</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.40.3 **Music** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Music</td></tr><tr><td>Technical name</td><td>music</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e5-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.41 Field **background\_music**

##### 2.1.2.1.3.41.1 **background\_music** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>background_music</td></tr><tr><td>Technical name</td><td>background_music</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e6-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.42 Field **dj**

##### 2.1.2.1.3.42.1 **dj** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>dj</td></tr><tr><td>Technical name</td><td>dj</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e7-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.43 Field **jukebox**

##### 2.1.2.1.3.43.1 **jukebox** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>jukebox</td></tr><tr><td>Technical name</td><td>jukebox</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e8-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.44 Field **karaoke**

##### 2.1.2.1.3.44.1 **karaoke** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>karaoke</td></tr><tr><td>Technical name</td><td>karaoke</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811e9-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.45 Field **live**

##### 2.1.2.1.3.45.1 **live** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>live</td></tr><tr><td>Technical name</td><td>live</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ea-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.46 Field **video**

##### 2.1.2.1.3.46.1 **video** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>video</td></tr><tr><td>Technical name</td><td>video</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811eb-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.47 Field **Noise Level**

##### 2.1.2.1.3.47.1 **Noise Level** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Noise Level</td></tr><tr><td>Technical name</td><td>noiseLevel</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ec-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.48 Field **Open 24 Hours**

##### 2.1.2.1.3.48.1 **Open 24 Hours** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Open 24 Hours</td></tr><tr><td>Technical name</td><td>open24Hours</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ed-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.49 Field **Order at Counter**

##### 2.1.2.1.3.49.1 **Order at Counter** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Order at Counter</td></tr><tr><td>Technical name</td><td>orderAtCounter</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ee-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.50 Field **Outdoor Seating**

##### 2.1.2.1.3.50.1 **Outdoor Seating** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Outdoor Seating</td></tr><tr><td>Technical name</td><td>outdoorSeating</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811ef-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.51 Field **Parking**

##### 2.1.2.1.3.51.1 **Parking** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image9.png?raw=true)

##### 2.1.2.1.3.51.2 **Parking** Hierarchy

Parent field: **attributes**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811f0-2b24-11e6-b7e5-591297143e36>garage</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f1-2b24-11e6-b7e5-591297143e36>lot</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f2-2b24-11e6-b7e5-591297143e36>street</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f3-2b24-11e6-b7e5-591297143e36>valet</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd811f4-2b24-11e6-b7e5-591297143e36>validated</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.51.3 **Parking** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Parking</td></tr><tr><td>Technical name</td><td>parking</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f0-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.52 Field **garage**

##### 2.1.2.1.3.52.1 **garage** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>garage</td></tr><tr><td>Technical name</td><td>garage</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f1-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.53 Field **lot**

##### 2.1.2.1.3.53.1 **lot** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>lot</td></tr><tr><td>Technical name</td><td>lot</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f2-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.54 Field **street**

##### 2.1.2.1.3.54.1 **street** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>street</td></tr><tr><td>Technical name</td><td>street</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f3-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.55 Field **valet**

##### 2.1.2.1.3.55.1 **valet** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>valet</td></tr><tr><td>Technical name</td><td>valet</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f4-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.56 Field **validated**

##### 2.1.2.1.3.56.1 **validated** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>validated</td></tr><tr><td>Technical name</td><td>validated</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f5-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.57 Field **Price Range**

##### 2.1.2.1.3.57.1 **Price Range** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Price Range</td></tr><tr><td>Technical name</td><td>priceRange</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f6-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.58 Field **Smoking**

##### 2.1.2.1.3.58.1 **Smoking** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Smoking</td></tr><tr><td>Technical name</td><td>smoking</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f7-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.59 Field **Take-out**

##### 2.1.2.1.3.59.1 **Take-out** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Take-out</td></tr><tr><td>Technical name</td><td>take-out</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f8-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.60 Field **Takes Reservations**

##### 2.1.2.1.3.60.1 **Takes Reservations** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Takes Reservations</td></tr><tr><td>Technical name</td><td>takesReservations</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811f9-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.61 Field **Waiter Service**

##### 2.1.2.1.3.61.1 **Waiter Service** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Waiter Service</td></tr><tr><td>Technical name</td><td>waiterService</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fa-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.62 Field **Wheelchair Accessible**

##### 2.1.2.1.3.62.1 **Wheelchair Accessible** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wheelchair Accessible</td></tr><tr><td>Technical name</td><td>wheelchairAccessible</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fb-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.63 Field **Wi-Fi**

##### 2.1.2.1.3.63.1 **Wi-Fi** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wi-Fi</td></tr><tr><td>Technical name</td><td>wi-fi</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fd-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.64 Field **categories**

##### 2.1.2.1.3.64.1 **categories** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image10.png?raw=true)

##### 2.1.2.1.3.64.2 **categories** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd811fe-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.64.3 **categories** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>categories</td></tr><tr><td>Technical name</td><td>categories</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd811fe-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.65 Field **\[0\]**

##### 2.1.2.1.3.65.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81201-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.66 Field **hours**

##### 2.1.2.1.3.66.1 **hours** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image11.png?raw=true)

##### 2.1.2.1.3.66.2 **hours** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81202-2b24-11e6-b7e5-591297143e36>Friday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81205-2b24-11e6-b7e5-591297143e36>Monday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81208-2b24-11e6-b7e5-591297143e36>Saturday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120b-2b24-11e6-b7e5-591297143e36>Sunday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120e-2b24-11e6-b7e5-591297143e36>Thursday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81211-2b24-11e6-b7e5-591297143e36>Tuesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81214-2b24-11e6-b7e5-591297143e36>Wednesday</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.66.3 **hours** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hours</td></tr><tr><td>Technical name</td><td>hours</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81202-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.67 Field **Friday**

##### 2.1.2.1.3.67.1 **Friday** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image12.png?raw=true)

##### 2.1.2.1.3.67.2 **Friday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81203-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81204-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.67.3 **Friday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Friday</td></tr><tr><td>Technical name</td><td>friday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81203-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.68 Field **close**

##### 2.1.2.1.3.68.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Technical name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81204-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.69 Field **open**

##### 2.1.2.1.3.69.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81205-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.70 Field **Monday**

##### 2.1.2.1.3.70.1 **Monday** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image13.png?raw=true)

##### 2.1.2.1.3.70.2 **Monday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81206-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81207-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.70.3 **Monday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Monday</td></tr><tr><td>Technical name</td><td>monday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81206-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.71 Field **close**

##### 2.1.2.1.3.71.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Technical name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81207-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.72 Field **open**

##### 2.1.2.1.3.72.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81208-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.73 Field **Saturday**

##### 2.1.2.1.3.73.1 **Saturday** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image14.png?raw=true)

##### 2.1.2.1.3.73.2 **Saturday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81209-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120a-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.73.3 **Saturday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Saturday</td></tr><tr><td>Technical name</td><td>saturday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81209-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.74 Field **close**

##### 2.1.2.1.3.74.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Technical name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8120a-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.75 Field **open**

##### 2.1.2.1.3.75.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8120b-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.76 Field **Sunday**

##### 2.1.2.1.3.76.1 **Sunday** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image15.png?raw=true)

##### 2.1.2.1.3.76.2 **Sunday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8120c-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd8120d-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.76.3 **Sunday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Sunday</td></tr><tr><td>Technical name</td><td>sunday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8120c-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.77 Field **close**

##### 2.1.2.1.3.77.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Technical name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8120d-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.78 Field **open**

##### 2.1.2.1.3.78.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8120e-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.79 Field **Thursday**

##### 2.1.2.1.3.79.1 **Thursday** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image16.png?raw=true)

##### 2.1.2.1.3.79.2 **Thursday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8120f-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81210-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.79.3 **Thursday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Thursday</td></tr><tr><td>Technical name</td><td>thursday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8120f-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.80 Field **close**

##### 2.1.2.1.3.80.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Technical name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81210-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.81 Field **open**

##### 2.1.2.1.3.81.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81211-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.82 Field **Tuesday**

##### 2.1.2.1.3.82.1 **Tuesday** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image17.png?raw=true)

##### 2.1.2.1.3.82.2 **Tuesday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81212-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81213-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.82.3 **Tuesday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Tuesday</td></tr><tr><td>Technical name</td><td>tuesday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81212-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.83 Field **close**

##### 2.1.2.1.3.83.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Technical name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81213-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.84 Field **open**

##### 2.1.2.1.3.84.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81214-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.85 Field **Wednesday**

##### 2.1.2.1.3.85.1 **Wednesday** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image18.png?raw=true)

##### 2.1.2.1.3.85.2 **Wednesday** Hierarchy

Parent field: **hours**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd81215-2b24-11e6-b7e5-591297143e36>close</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0dd81216-2b24-11e6-b7e5-591297143e36>open</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.85.3 **Wednesday** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>Wednesday</td></tr><tr><td>Technical name</td><td>wednesday</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81215-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.86 Field **close**

##### 2.1.2.1.3.86.1 **close** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>close</td></tr><tr><td>Technical name</td><td>close</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81216-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.87 Field **open**

##### 2.1.2.1.3.87.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81217-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.88 Field **latitude**

##### 2.1.2.1.3.88.1 **latitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latitude</td></tr><tr><td>Technical name</td><td>latitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81218-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.89 Field **longitude**

##### 2.1.2.1.3.89.1 **longitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>longitude</td></tr><tr><td>Technical name</td><td>longitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121a-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.90 Field **neighborhoods**

##### 2.1.2.1.3.90.1 **neighborhoods** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image19.png?raw=true)

##### 2.1.2.1.3.90.2 **neighborhoods** Hierarchy

Parent field: **businesses**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0dd8121b-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.1.3.90.3 **neighborhoods** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>neighborhoods</td></tr><tr><td>Technical name</td><td>neighborhoods</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121b-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.91 Field **\[0\]**

##### 2.1.2.1.3.91.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121c-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.92 Field **open**

##### 2.1.2.1.3.92.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>boolean</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121d-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.93 Field **review\_count**

##### 2.1.2.1.3.93.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Technical name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd8121e-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.94 Field **stars**

##### 2.1.2.1.3.94.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Technical name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0dd81220-2b24-11e6-b7e5-591297143e36"></a>2.1.2.1.3.95 Field **type**

##### 2.1.2.1.3.95.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

##### 2.1.2.1.4 **businesses** Target Script

```
use yelp;

db.createCollection( "businesses",{
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "businesses",
            "properties": {
                "\_id": {
                    "bsonType": "objectId"
                },
                "business\_id": {
                    "bsonType": "objectId",
                    "description": "Unique key for businesses"
                },
                "name": {
                    "bsonType": "string"
                },
                "full\_address": {
                    "bsonType": "object",
                    "properties": {
                        "houseNum": {
                            "bsonType": "string"
                        },
                        "street": {
                            "bsonType": "string"
                        },
                        "box": {
                            "bsonType": "string"
                        },
                        "city": {
                            "bsonType": "string"
                        },
                        "state": {
                            "bsonType": "string"
                        },
                        "zip": {
                            "bsonType": "string"
                        }
                    },
                    "additionalProperties": false
                },
                "city": {
                    "bsonType": "string"
                },
                "state": {
                    "bsonType": "string"
                },
                "attributes": {
                    "bsonType": "object",
                    "properties": {
                        "acceptsCreditCards": {
                            "bsonType": "bool"
                        },
                        "acceptsInsurance": {
                            "bsonType": "bool"
                        },
                        "alcohol": {
                            "bsonType": "string"
                        },
                        "ambience": {
                            "bsonType": "object",
                            "properties": {
                                "casual": {
                                    "bsonType": "bool"
                                },
                                "classy": {
                                    "bsonType": "bool"
                                },
                                "divey": {
                                    "bsonType": "bool"
                                },
                                "hipster": {
                                    "bsonType": "bool"
                                },
                                "intimate": {
                                    "bsonType": "bool"
                                },
                                "romantic": {
                                    "bsonType": "bool"
                                },
                                "touristy": {
                                    "bsonType": "bool"
                                },
                                "trendy": {
                                    "bsonType": "bool"
                                },
                                "upscale": {
                                    "bsonType": "bool"
                                }
                            }
                        },
                        "attire": {
                            "bsonType": "string"
                        },
                        "byAppointmentOnly": {
                            "bsonType": "bool"
                        },
                        "byob/corkage": {
                            "bsonType": "string"
                        },
                        "caters": {
                            "bsonType": "bool"
                        },
                        "coatCheck": {
                            "bsonType": "bool"
                        },
                        "delivery": {
                            "bsonType": "bool"
                        },
                        "dogsAllowed": {
                            "bsonType": "bool"
                        },
                        "drive-thru": {
                            "bsonType": "bool"
                        },
                        "goodFor": {
                            "bsonType": "object",
                            "properties": {
                                "breakfast": {
                                    "bsonType": "bool"
                                },
                                "brunch": {
                                    "bsonType": "bool"
                                },
                                "dessert": {
                                    "bsonType": "bool"
                                },
                                "dinner": {
                                    "bsonType": "bool"
                                },
                                "latenight": {
                                    "bsonType": "bool"
                                },
                                "lunch": {
                                    "bsonType": "bool"
                                }
                            }
                        },
                        "goodForDancing": {
                            "bsonType": "bool"
                        },
                        "goodForGroups": {
                            "bsonType": "bool"
                        },
                        "goodForKids": {
                            "bsonType": "bool"
                        },
                        "happyHour": {
                            "bsonType": "bool"
                        },
                        "hasTv": {
                            "bsonType": "bool"
                        },
                        "music": {
                            "bsonType": "object",
                            "properties": {
                                "background\_music": {
                                    "bsonType": "bool"
                                },
                                "dj": {
                                    "bsonType": "bool"
                                },
                                "jukebox": {
                                    "bsonType": "bool"
                                },
                                "karaoke": {
                                    "bsonType": "bool"
                                },
                                "live": {
                                    "bsonType": "bool"
                                },
                                "video": {
                                    "bsonType": "bool"
                                }
                            }
                        },
                        "noiseLevel": {
                            "bsonType": "string"
                        },
                        "open24Hours": {
                            "bsonType": "bool"
                        },
                        "orderAtCounter": {
                            "bsonType": "bool"
                        },
                        "outdoorSeating": {
                            "bsonType": "bool"
                        },
                        "parking": {
                            "bsonType": "object",
                            "properties": {
                                "garage": {
                                    "bsonType": "bool"
                                },
                                "lot": {
                                    "bsonType": "bool"
                                },
                                "street": {
                                    "bsonType": "bool"
                                },
                                "valet": {
                                    "bsonType": "bool"
                                },
                                "validated": {
                                    "bsonType": "bool"
                                }
                            }
                        },
                        "priceRange": {
                            "bsonType": "number"
                        },
                        "smoking": {
                            "bsonType": "string"
                        },
                        "take-out": {
                            "bsonType": "bool"
                        },
                        "takesReservations": {
                            "bsonType": "bool"
                        },
                        "waiterService": {
                            "bsonType": "bool"
                        },
                        "wheelchairAccessible": {
                            "bsonType": "bool"
                        },
                        "wi-fi": {
                            "bsonType": "string"
                        }
                    }
                },
                "categories": {
                    "bsonType": "array",
                    "items": {
                        "bsonType": "string"
                    }
                },
                "hours": {
                    "bsonType": "object",
                    "properties": {
                        "friday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            }
                        },
                        "monday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            }
                        },
                        "saturday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            }
                        },
                        "sunday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            }
                        },
                        "thursday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            }
                        },
                        "tuesday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            }
                        },
                        "wednesday": {
                            "bsonType": "object",
                            "properties": {
                                "close": {
                                    "bsonType": "string"
                                },
                                "open": {
                                    "bsonType": "string"
                                }
                            }
                        }
                    }
                },
                "latitude": {
                    "bsonType": "number"
                },
                "longitude": {
                    "bsonType": "number"
                },
                "neighborhoods": {
                    "bsonType": "array",
                    "items": {
                        "bsonType": "string"
                    }
                },
                "open": {
                    "bsonType": "bool"
                },
                "review\_count": {
                    "bsonType": "number"
                },
                "stars": {
                    "bsonType": "number"
                },
                "type": {
                    "bsonType": "string"
                }
            },
            "required": \[
                "business\_id"
            \]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn"
});

```

### <a id="a080d1d0-91f6-11e9-a924-ddc9cd9b071f"></a>2.1.2.2 Collection **checkins**

##### 2.1.2.2.1 **checkins** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image20.png?raw=true)

##### 2.1.2.2.2 **checkins** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>checkins</td></tr><tr><td>Technical name</td><td>checkins</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Id</td><td></td></tr><tr><td>Description</td><td><div class="docs-markdown"></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6>yelp</a></td></tr><tr><td>Capped</td><td></td></tr><tr><td>Size</td><td></td></tr><tr><td>Max</td><td></td></tr><tr><td>Storage engine</td><td></td></tr><tr><td>Validation level</td><td></td></tr><tr><td>Validation action</td><td></td></tr><tr><td>Additional properties</td><td></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Custom property</td><td></td></tr></tbody></table>

##### 2.1.2.2.3 **checkins** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#9c7dc020-91f6-11e9-a924-ddc9cd9b071f>\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7dc022-91f6-11e9-a924-ddc9cd9b071f>checkin\_info</a></td><td class="no-break-word">document</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e76-91f6-11e9-a924-ddc9cd9b071f>^\[a-zA-Z0-9\_.-\]{3}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e45-91f6-11e9-a924-ddc9cd9b071f>^\[a-zA-Z0-9\_.-\]{4}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e77-91f6-11e9-a924-ddc9cd9b071f>type</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f>business\_id</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="9c7dc020-91f6-11e9-a924-ddc9cd9b071f"></a>2.1.2.2.3.1 Field **\_id**

##### 2.1.2.2.3.1.1 **\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>_id</td></tr><tr><td>Technical name</td><td>_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="9c7dc022-91f6-11e9-a924-ddc9cd9b071f"></a>2.1.2.2.3.2 Field **checkin\_info**

##### 2.1.2.2.3.2.1 **checkin\_info** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image21.png?raw=true)

##### 2.1.2.2.3.2.2 **checkin\_info** Hierarchy

Parent field: **checkins**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#9c7e0e76-91f6-11e9-a924-ddc9cd9b071f>^\[a-zA-Z0-9\_.-\]{3}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9c7e0e45-91f6-11e9-a924-ddc9cd9b071f>^\[a-zA-Z0-9\_.-\]{4}$</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.2.3.2.3 **checkin\_info** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>checkin_info</td></tr><tr><td>Technical name</td><td>checkin_info</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e76-91f6-11e9-a924-ddc9cd9b071f"></a>2.1.2.2.3.3 Field **^\[a-zA-Z0-9\_.-\]{3}$**

##### 2.1.2.2.3.3.1 **^\[a-zA-Z0-9\_.-\]{3}$** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>^[a-zA-Z0-9_.-]{3}$</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Sample Name</td><td>9-6</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Excl min</td><td>false</td></tr><tr><td>Excl max</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e45-91f6-11e9-a924-ddc9cd9b071f"></a>2.1.2.2.3.4 Field **^\[a-zA-Z0-9\_.-\]{4}$**

##### 2.1.2.2.3.4.1 **^\[a-zA-Z0-9\_.-\]{4}$** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>^[a-zA-Z0-9_.-]{4}$</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Sample Name</td><td>23-6</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Excl min</td><td>false</td></tr><tr><td>Excl max</td><td>false</td></tr></tbody></table>

### <a id="9c7e0e77-91f6-11e9-a924-ddc9cd9b071f"></a>2.1.2.2.3.5 Field **type**

##### 2.1.2.2.3.5.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>checkin</td></tr></tbody></table>

### <a id="9c7dc021-91f6-11e9-a924-ddc9cd9b071f"></a>2.1.2.2.3.6 Field **business\_id**

##### 2.1.2.2.3.6.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Foreign collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Foreign field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr><tr><td>Sample</td><td>eFA9dqXT5EA_TrMgbo03QQ</td></tr></tbody></table>

##### 2.1.2.2.4 **checkins** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">_id_</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">_id_</td></tr><tr><td>Key</td><td class="table-column-indexes">_id('ascending')</td></tr><tr><td>Hashed</td><td class="table-column-indexes"></td></tr><tr><td>Unique</td><td class="table-column-indexes"></td></tr><tr><td>Drop duplicates</td><td class="table-column-indexes"></td></tr><tr><td>Sparse</td><td class="table-column-indexes"></td></tr><tr><td>Background indexing</td><td class="table-column-indexes"></td></tr><tr><td>Partial filter exp</td><td class="table-column-indexes"></td></tr><tr><td>Expire after (seconds)</td><td class="table-column-indexes"></td></tr><tr><td>Storage engine</td><td class="table-column-indexes"></td></tr><tr><td>Comments</td><td class="table-column-indexes"></td></tr><tr><td>Custom index property</td><td class="table-column-indexes"></td></tr></tbody></table>

##### 2.1.2.2.5 **checkins** Target Script

```
use yelp;

db.createCollection( "checkins",{
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "checkins",
            "properties": {
                "\_id": {
                    "bsonType": "objectId"
                },
                "checkin\_info": {
                    "bsonType": "object",
                    "additionalProperties": false,
                    "patternProperties": {
                        "^\[a-zA-Z0-9\_.-\]{3}$": {
                            "bsonType": "number"
                        },
                        "^\[a-zA-Z0-9\_.-\]{4}$": {
                            "bsonType": "number"
                        }
                    }
                },
                "type": {
                    "bsonType": "string"
                },
                "business\_id": {
                    "bsonType": "string"
                }
            },
            "required": \[
                "\_id",
                "checkin\_info",
                "type",
                "business\_id"
            \]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn"
});
db.checkins.createIndex(
{
    "\_id": 1
},
{
    "name": "\_id\_"
}
);

```

### <a id="0da2aa00-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3 Collection **reviews**

##### 2.1.2.3.1 **reviews** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image22.png?raw=true)

##### 2.1.2.3.2 **reviews** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>reviews</td></tr><tr><td>Technical name</td><td>reviews</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Id</td><td></td></tr><tr><td>Description</td><td><div class="docs-markdown"></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6>yelp</a></td></tr><tr><td>Capped</td><td></td></tr><tr><td>Size</td><td></td></tr><tr><td>Max</td><td></td></tr><tr><td>Storage engine</td><td></td></tr><tr><td>Validation level</td><td></td></tr><tr><td>Validation action</td><td></td></tr><tr><td>Additional properties</td><td></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Custom property</td><td></td></tr></tbody></table>

##### 2.1.2.3.3 **reviews** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0da2aa04-2b24-11e6-b7e5-591297143e36>review\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36>business\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa03-2b24-11e6-b7e5-591297143e36>date</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa05-2b24-11e6-b7e5-591297143e36>stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa06-2b24-11e6-b7e5-591297143e36>text</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa07-2b24-11e6-b7e5-591297143e36>type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36>user\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa09-2b24-11e6-b7e5-591297143e36>votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0a-2b24-11e6-b7e5-591297143e36>cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0b-2b24-11e6-b7e5-591297143e36>funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0c-2b24-11e6-b7e5-591297143e36>useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0da2aa04-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.1 Field **review\_id**

##### 2.1.2.3.3.1.1 **review\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_id</td></tr><tr><td>Technical name</td><td>review_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0da2aa02-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.2 Field **business\_id**

##### 2.1.2.3.3.2.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0da2aa03-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.3 Field **date**

##### 2.1.2.3.3.3.1 **date** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>date</td></tr><tr><td>Technical name</td><td>date</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0da2aa05-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.4 Field **stars**

##### 2.1.2.3.3.4.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Technical name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0da2aa06-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.5 Field **text**

##### 2.1.2.3.3.5.1 **text** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>text</td></tr><tr><td>Technical name</td><td>text</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0da2aa07-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.6 Field **type**

##### 2.1.2.3.3.6.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0da2aa08-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.7 Field **user\_id**

##### 2.1.2.3.3.7.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Technical name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0da2aa09-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.8 Field **votes**

##### 2.1.2.3.3.8.1 **votes** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image23.png?raw=true)

##### 2.1.2.3.3.8.2 **votes** Hierarchy

Parent field: **reviews**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0da2aa0a-2b24-11e6-b7e5-591297143e36>cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0b-2b24-11e6-b7e5-591297143e36>funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0da2aa0c-2b24-11e6-b7e5-591297143e36>useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.3.3.8.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Technical name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0da2aa0a-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.9 Field **cool**

##### 2.1.2.3.3.9.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Technical name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0da2aa0b-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.10 Field **funny**

##### 2.1.2.3.3.10.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Technical name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0da2aa0c-2b24-11e6-b7e5-591297143e36"></a>2.1.2.3.3.11 Field **useful**

##### 2.1.2.3.3.11.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Technical name</td><td>useful</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

##### 2.1.2.3.4 **reviews** Target Script

```
use yelp;

db.createCollection( "reviews",{
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "reviews",
            "properties": {
                "\_id": {
                    "bsonType": "objectId"
                },
                "review\_id": {
                    "bsonType": "objectId"
                },
                "business\_id": {
                    "bsonType": "objectId"
                },
                "date": {
                    "bsonType": "string"
                },
                "stars": {
                    "bsonType": "number"
                },
                "text": {
                    "bsonType": "string"
                },
                "type": {
                    "bsonType": "string"
                },
                "user\_id": {
                    "bsonType": "objectId"
                },
                "votes": {
                    "bsonType": "object",
                    "properties": {
                        "cool": {
                            "bsonType": "number"
                        },
                        "funny": {
                            "bsonType": "number"
                        },
                        "useful": {
                            "bsonType": "number"
                        }
                    }
                }
            },
            "required": \[
                "review\_id",
                "business\_id",
                "user\_id"
            \]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn"
});

```

### <a id="0de02830-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4 Collection **tips**

##### 2.1.2.4.1 **tips** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image24.png?raw=true)

##### 2.1.2.4.2 **tips** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>tips</td></tr><tr><td>Technical name</td><td>tips</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Id</td><td></td></tr><tr><td>Description</td><td><div class="docs-markdown"></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6>yelp</a></td></tr><tr><td>Capped</td><td></td></tr><tr><td>Size</td><td></td></tr><tr><td>Max</td><td></td></tr><tr><td>Storage engine</td><td></td></tr><tr><td>Validation level</td><td></td></tr><tr><td>Validation action</td><td></td></tr><tr><td>Additional properties</td><td></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Custom property</td><td></td></tr></tbody></table>

##### 2.1.2.4.3 **tips** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0de02831-2b24-11e6-b7e5-591297143e36>\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36>business\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02833-2b24-11e6-b7e5-591297143e36>date</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02834-2b24-11e6-b7e5-591297143e36>likes</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02835-2b24-11e6-b7e5-591297143e36>text</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02836-2b24-11e6-b7e5-591297143e36>type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36>user\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0de02831-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4.3.1 Field **\_id**

##### 2.1.2.4.3.1.1 **\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>_id</td></tr><tr><td>Technical name</td><td>_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0de02832-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4.3.2 Field **business\_id**

##### 2.1.2.4.3.2.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

### <a id="0de02833-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4.3.3 Field **date**

##### 2.1.2.4.3.3.1 **date** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>date</td></tr><tr><td>Technical name</td><td>date</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0de02834-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4.3.4 Field **likes**

##### 2.1.2.4.3.4.1 **likes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>likes</td></tr><tr><td>Technical name</td><td>likes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0de02835-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4.3.5 Field **text**

##### 2.1.2.4.3.5.1 **text** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>text</td></tr><tr><td>Technical name</td><td>text</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0de02836-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4.3.6 Field **type**

##### 2.1.2.4.3.6.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0de02837-2b24-11e6-b7e5-591297143e36"></a>2.1.2.4.3.7 Field **user\_id**

##### 2.1.2.4.3.7.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Technical name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Relationship type</td><td>Foreign Key</td></tr></tbody></table>

##### 2.1.2.4.4 **tips** Target Script

```
use yelp;

db.createCollection( "tips",{
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "tips",
            "properties": {
                "\_id": {
                    "bsonType": "objectId"
                },
                "business\_id": {
                    "bsonType": "objectId"
                },
                "date": {
                    "bsonType": "string"
                },
                "likes": {
                    "bsonType": "number"
                },
                "text": {
                    "bsonType": "string"
                },
                "type": {
                    "bsonType": "string"
                },
                "user\_id": {
                    "bsonType": "objectId"
                }
            },
            "required": \[
                "\_id",
                "business\_id",
                "user\_id"
            \]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn"
});

```

### <a id="0df0f110-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5 Collection **users**

##### 2.1.2.5.1 **users** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image25.png?raw=true)

##### 2.1.2.5.2 **users** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Collection name</td><td>users</td></tr><tr><td>Technical name</td><td>users</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Id</td><td></td></tr><tr><td>Description</td><td><div class="docs-markdown"><p>Users description</p></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6>yelp</a></td></tr><tr><td>Capped</td><td></td></tr><tr><td>Size</td><td></td></tr><tr><td>Max</td><td></td></tr><tr><td>Storage engine</td><td></td></tr><tr><td>Validation level</td><td></td></tr><tr><td>Validation action</td><td></td></tr><tr><td>Additional properties</td><td></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Custom property</td><td></td></tr></tbody></table>

##### 2.1.2.5.3 **users** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user\_id</a></td><td class="no-break-word">objectId</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f125-2b24-11e6-b7e5-591297143e36>type</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f123-2b24-11e6-b7e5-591297143e36>name</a></td><td class="no-break-word">string</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr><td><a href=#0df0f112-2b24-11e6-b7e5-591297143e36>average\_stars</a></td><td class="no-break-word">numeric</td><td>true</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f113-2b24-11e6-b7e5-591297143e36>compliments</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36>cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36>cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36>funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36>hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f118-2b24-11e6-b7e5-591297143e36>more</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36>note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36>photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36>plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36>profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36>writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11e-2b24-11e6-b7e5-591297143e36>elite</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f120-2b24-11e6-b7e5-591297143e36>fans</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f121-2b24-11e6-b7e5-591297143e36>friends</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f124-2b24-11e6-b7e5-591297143e36>review\_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f127-2b24-11e6-b7e5-591297143e36>votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36>cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36>funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36>useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12b-2b24-11e6-b7e5-591297143e36>yelping\_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="0df0f126-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.1 Field **user\_id**

##### 2.1.2.5.3.1.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Technical name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>objectId</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>true</td></tr></tbody></table>

### <a id="0df0f125-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.2 Field **type**

##### 2.1.2.5.3.2.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Enum</td><td>user,owner,tester</td></tr></tbody></table>

### <a id="0df0f123-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.3 Field **name**

##### 2.1.2.5.3.3.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Sample</td><td>jkHFSDKNFDS?FN</td></tr><tr><td>Comments</td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr><td>Privacy-concerned</td><td>true</td></tr><tr><td>GDPR classification</td><td>Confidential</td></tr></tbody></table>

### <a id="0df0f112-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.4 Field **average\_stars**

##### 2.1.2.5.3.4.1 **average\_stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>average_stars</td></tr><tr><td>Technical name</td><td>average_stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>true</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Unit</td><td>stars</td></tr><tr><td>Min value</td><td>1</td></tr><tr><td>Excl min</td><td>false</td></tr><tr><td>Max value</td><td>5</td></tr><tr><td>Excl max</td><td>true</td></tr><tr><td>Sample</td><td>3</td></tr></tbody></table>

### <a id="0df0f113-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.5 Field **compliments**

##### 2.1.2.5.3.5.1 **compliments** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image26.png?raw=true)

##### 2.1.2.5.3.5.2 **compliments** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f114-2b24-11e6-b7e5-591297143e36>cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f115-2b24-11e6-b7e5-591297143e36>cute</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f116-2b24-11e6-b7e5-591297143e36>funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f117-2b24-11e6-b7e5-591297143e36>hot</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f118-2b24-11e6-b7e5-591297143e36>more</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f119-2b24-11e6-b7e5-591297143e36>note</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11a-2b24-11e6-b7e5-591297143e36>photos</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11b-2b24-11e6-b7e5-591297143e36>plain</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11c-2b24-11e6-b7e5-591297143e36>profile</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f11d-2b24-11e6-b7e5-591297143e36>writer</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.5.3.5.3 **compliments** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>compliments</td></tr><tr><td>Technical name</td><td>compliments</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f114-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.6 Field **cool**

##### 2.1.2.5.3.6.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Technical name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f115-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.7 Field **cute**

##### 2.1.2.5.3.7.1 **cute** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cute</td></tr><tr><td>Technical name</td><td>cute</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f116-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.8 Field **funny**

##### 2.1.2.5.3.8.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Technical name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f117-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.9 Field **hot**

##### 2.1.2.5.3.9.1 **hot** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>hot</td></tr><tr><td>Technical name</td><td>hot</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f118-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.10 Field **more**

##### 2.1.2.5.3.10.1 **more** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>more</td></tr><tr><td>Technical name</td><td>more</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f119-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.11 Field **note**

##### 2.1.2.5.3.11.1 **note** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>note</td></tr><tr><td>Technical name</td><td>note</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f11a-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.12 Field **photos**

##### 2.1.2.5.3.12.1 **photos** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>photos</td></tr><tr><td>Technical name</td><td>photos</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f11b-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.13 Field **plain**

##### 2.1.2.5.3.13.1 **plain** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>plain</td></tr><tr><td>Technical name</td><td>plain</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f11c-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.14 Field **profile**

##### 2.1.2.5.3.14.1 **profile** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>profile</td></tr><tr><td>Technical name</td><td>profile</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f11d-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.15 Field **writer**

##### 2.1.2.5.3.15.1 **writer** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>writer</td></tr><tr><td>Technical name</td><td>writer</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f11e-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.16 Field **elite**

##### 2.1.2.5.3.16.1 **elite** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image27.png?raw=true)

##### 2.1.2.5.3.16.2 **elite** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f11f-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.5.3.16.3 **elite** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>elite</td></tr><tr><td>Technical name</td><td>elite</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="0df0f11f-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.17 Field **\[0\]**

##### 2.1.2.5.3.17.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f120-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.18 Field **fans**

##### 2.1.2.5.3.18.1 **fans** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fans</td></tr><tr><td>Technical name</td><td>fans</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f121-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.19 Field **friends**

##### 2.1.2.5.3.19.1 **friends** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image28.png?raw=true)

##### 2.1.2.5.3.19.2 **friends** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f122-2b24-11e6-b7e5-591297143e36>\[0\]</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.5.3.19.3 **friends** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>friends</td></tr><tr><td>Technical name</td><td>friends</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="0df0f122-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.20 Field **\[0\]**

##### 2.1.2.5.3.20.1 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f124-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.21 Field **review\_count**

##### 2.1.2.5.3.21.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Technical name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f127-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.22 Field **votes**

##### 2.1.2.5.3.22.1 **votes** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image29.png?raw=true)

##### 2.1.2.5.3.22.2 **votes** Hierarchy

Parent field: **users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36>cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36>funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36>useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 2.1.2.5.3.22.3 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Technical name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f128-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.23 Field **cool**

##### 2.1.2.5.3.23.1 **cool** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>cool</td></tr><tr><td>Technical name</td><td>cool</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f129-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.24 Field **funny**

##### 2.1.2.5.3.24.1 **funny** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>funny</td></tr><tr><td>Technical name</td><td>funny</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f12a-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.25 Field **useful**

##### 2.1.2.5.3.25.1 **useful** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>useful</td></tr><tr><td>Technical name</td><td>useful</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>numeric</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

### <a id="0df0f12b-2b24-11e6-b7e5-591297143e36"></a>2.1.2.5.3.26 Field **yelping\_since**

##### 2.1.2.5.3.26.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Technical name</td><td>yelping_since</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>string</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr></tbody></table>

##### 2.1.2.5.4 **users** Users (TBD)

<table><thead><tr><td>Username</td><td>Read</td><td>Read Write</td><td>Custom user property</td></tr></thead><tbody><tr><td>New User</td><td>false</td><td>false</td><td></td></tr></tbody></table>

##### 2.1.2.5.5 **users** Indexes

<table class="index-table"><thead><tr><td class="table-property-column">Property</td><td class="table-column-property">name+stars</td><td class="table-column-property">New Index1</td></tr></thead><tbody><tr><td>Name</td><td class="table-column-indexes">name+stars</td><td class="table-column-indexes">New Index1</td></tr><tr><td>Key</td><td class="table-column-indexes">name('ascending'), average_stars('descending')</td><td class="table-column-indexes">writer('ascending')</td></tr><tr><td>Hashed</td><td class="table-column-indexes"></td><td class="table-column-indexes"></td></tr><tr><td>Unique</td><td class="table-column-indexes"></td><td class="table-column-indexes"></td></tr><tr><td>Drop duplicates</td><td class="table-column-indexes"></td><td class="table-column-indexes"></td></tr><tr><td>Sparse</td><td class="table-column-indexes"></td><td class="table-column-indexes">true</td></tr><tr><td>Background indexing</td><td class="table-column-indexes"></td><td class="table-column-indexes">true</td></tr><tr><td>Partial filter exp</td><td class="table-column-indexes"></td><td class="table-column-indexes"></td></tr><tr><td>Expire after (seconds)</td><td class="table-column-indexes"></td><td class="table-column-indexes"></td></tr><tr><td>Storage engine</td><td class="table-column-indexes">WiredTiger</td><td class="table-column-indexes">WiredTiger</td></tr><tr><td>Comments</td><td class="table-column-indexes"></td><td class="table-column-indexes"></td></tr><tr><td>Custom index property</td><td class="table-column-indexes"></td><td class="table-column-indexes"></td></tr></tbody></table>

##### 2.1.2.5.6 **users** Sharding

<table><thead><tr><td>Property</td><td>Sharding</td></tr></thead><tbody><tr><td>Key</td><td>name+stars</td></tr><tr><td>Hashed</td><td></td></tr><tr><td>Unique</td><td>true</td></tr><tr><td>Number of initial chunks</td><td></td></tr><tr><td>Collation</td><td>null</td></tr><tr><td>Zone (Tag)</td><td></td></tr><tr><td>Comments</td><td></td></tr><tr><td>Custom sharding property</td><td></td></tr></tbody></table>

##### 2.1.2.5.7 **users** Target Script

```
use yelp;

db.createCollection( "users",{
    "capped": false,
    "validator": {
        "$jsonSchema": {
            "bsonType": "object",
            "title": "users",
            "description": "Users description",
            "properties": {
                "\_id": {
                    "bsonType": "objectId"
                },
                "user\_id": {
                    "bsonType": "objectId"
                },
                "type": {
                    "bsonType": "string",
                    "enum": \[
                        "user",
                        "owner",
                        "tester"
                    \]
                },
                "name": {
                    "bsonType": "string"
                },
                "average\_stars": {
                    "bsonType": "number",
                    "minimum": 1,
                    "maximum": 5,
                    "exclusiveMaximum": true
                },
                "compliments": {
                    "bsonType": "object",
                    "properties": {
                        "cool": {
                            "bsonType": "number"
                        },
                        "cute": {
                            "bsonType": "number"
                        },
                        "funny": {
                            "bsonType": "number"
                        },
                        "hot": {
                            "bsonType": "number"
                        },
                        "more": {
                            "bsonType": "number"
                        },
                        "note": {
                            "bsonType": "number"
                        },
                        "photos": {
                            "bsonType": "number"
                        },
                        "plain": {
                            "bsonType": "number"
                        },
                        "profile": {
                            "bsonType": "number"
                        },
                        "writer": {
                            "bsonType": "number"
                        }
                    }
                },
                "elite": {
                    "bsonType": "array",
                    "additionalItems": true,
                    "items": {
                        "bsonType": "number"
                    }
                },
                "fans": {
                    "bsonType": "number"
                },
                "friends": {
                    "bsonType": "array",
                    "additionalItems": true,
                    "items": {
                        "bsonType": "string"
                    }
                },
                "review\_count": {
                    "bsonType": "number"
                },
                "votes": {
                    "bsonType": "object",
                    "properties": {
                        "cool": {
                            "bsonType": "number"
                        },
                        "funny": {
                            "bsonType": "number"
                        },
                        "useful": {
                            "bsonType": "number"
                        }
                    }
                },
                "yelping\_since": {
                    "bsonType": "string"
                }
            },
            "required": \[
                "user\_id",
                "type",
                "name",
                "average\_stars"
            \]
        }
    },
    "validationLevel": "off",
    "validationAction": "warn"
});
db.users.createIndex(
{
    "name": 1,
    "average\_stars": -1
},
{
    "name": "name+stars"
}
);
db.users.createIndex(
{
    "compliments.writer": 1
},
{
    "name": "New Index1",
    "sparse": true,
    "background": true
}
);


/\*Add sharding script\*/
sh.enableSharding("yelp");
sh.shardCollection("yelp.users",
{
    "name+stars": 1
},
true,
{});
```

### <a id="views"></a>

##### 3\. Views

### <a id="5c771580-5193-11e7-b9f2-49270a53df2c"></a>3.1 View **rov\_bussiness**

##### 3.1.1 **rov\_bussiness** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image30.png?raw=true)

##### 3.1.2 **rov\_bussiness** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>View name</td><td>rov_bussiness</td></tr><tr><td>Technical name</td><td>rov_bussiness</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Id</td><td></td></tr><tr><td>Description</td><td><div class="docs-markdown"></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6>yelp</a></td></tr><tr><td>View on</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Pipeline</td><td>[ { "$project": { "business_id": 1, "name": 1, "full_address": { "houseNum": "$full_address.houseNum", "street": "$full_address.street", "box": "$full_address.box", "city": "$full_address.city", "state": "$full_address.state", "zip": "$full_address.zip" }, "type": 1 } } ]</td></tr><tr><td>Additional properties</td><td></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Simple text</td><td></td></tr></tbody></table>

##### 3.1.3 **rov\_bussiness** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#97c2fc30-5193-11e7-b9f2-49270a53df2c>business\_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr><tr><td><a href=#67601810-5194-11e7-b9f2-49270a53df2c>name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#a08b5e20-5193-11e7-b9f2-49270a53df2c>full\_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7107ebf0-dc5b-11e9-b819-e3f2d5171928>houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#760da090-dc5b-11e9-b819-e3f2d5171928>street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7bfbe070-dc5b-11e9-b819-e3f2d5171928>box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7ee803e0-dc5b-11e9-b819-e3f2d5171928>city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#85787730-dc5b-11e9-b819-e3f2d5171928>state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#87afc990-dc5b-11e9-b819-e3f2d5171928>zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#704306e0-5194-11e7-b9f2-49270a53df2c>type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="97c2fc30-5193-11e7-b9f2-49270a53df2c"></a>3.1.3.1 Field **business\_id**

##### 3.1.3.1.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="67601810-5194-11e7-b9f2-49270a53df2c"></a>3.1.3.2 Field **name**

##### 3.1.3.2.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="a08b5e20-5193-11e7-b9f2-49270a53df2c"></a>3.1.3.3 Field **full\_address**

##### 3.1.3.3.1 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Technical name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="704306e0-5194-11e7-b9f2-49270a53df2c"></a>3.1.3.4 Field **type**

##### 3.1.3.4.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="090874c0-5206-11e7-8e65-9b1d6a151b1d"></a>3.2 View **rov\_rev\_users**

##### 3.2.1 **rov\_rev\_users** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image31.png?raw=true)

##### 3.2.2 **rov\_rev\_users** Properties

<table class="collection-properties-table"><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>View name</td><td>rov_rev_users</td></tr><tr><td>Technical name</td><td>rov_rev_users</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Id</td><td></td></tr><tr><td>Description</td><td><div class="docs-markdown"></div></td></tr><tr><td>Database</td><td><a href=#3dee5aa0-f5dc-11e6-aaa0-997d0683e5e6>yelp</a></td></tr><tr><td>View on</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Pipeline</td><td>[ { "$project": { "review_id": 1, "date": 1, "stars": 1, "type": 1, "business": { "business_id": "$business_id", "name": "$name", "type": "$type", "open": "$open", "stars": "$stars", "review_count": "$review_count", "full_address": { "houseNum": "$full_address.houseNum", "street": "$full_address.street", "box": "$full_address.box", "city": "$full_address.city", "state": "$full_address.state", "zip": "$full_address.zip" }, "city": "$city", "state": "$state", "latitude": "$latitude", "longitude": "$longitude" }, "user": { "user_id": "$user_id", "name": "$name", "type": "$type", "votes": { "cool": "$votes.cool", "funny": "$votes.funny", "useful": "$votes.useful" }, "yelping_since": "$yelping_since" } } }, { "$lookup": { "from": "businesses", "as": "business", "localField": "business_id", "foreignField": "_id" } }, { "$lookup": { "from": "users", "as": "username", "localField": "user_id", "foreignField": "name" } } ]</td></tr><tr><td>Additional properties</td><td></td></tr><tr><td>Comments</td><td><div class="docs-markdown"></div></td></tr><tr><td>Simple text</td><td></td></tr></tbody></table>

##### 3.2.3 **rov\_rev\_users** Fields

<table><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#70972f00-5210-11e7-8e65-9b1d6a151b1d>review\_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#81b90470-5210-11e7-8e65-9b1d6a151b1d>date</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#8eefbd00-5210-11e7-8e65-9b1d6a151b1d>stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#9aadb840-5210-11e7-8e65-9b1d6a151b1d>type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78ca5f0-520d-11e7-8e65-9b1d6a151b1d>business</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e0580-520d-11e7-8e65-9b1d6a151b1d>\[0\]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c92-520d-11e7-8e65-9b1d6a151b1d>business\_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"><p>Unique key for businesses</p></div></td><td><div class="docs-markdown"><p>Sat Nov 04 2017 10:12:00 GMT+0100 (Romance Standard Time): some comments</p></div></td></tr><tr><td><a href=#b78e2c99-520d-11e7-8e65-9b1d6a151b1d>name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9f-520d-11e7-8e65-9b1d6a151b1d>type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9b-520d-11e7-8e65-9b1d6a151b1d>open</a></td><td class="no-break-word">boolean</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9d-520d-11e7-8e65-9b1d6a151b1d>stars</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9c-520d-11e7-8e65-9b1d6a151b1d>review\_count</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c95-520d-11e7-8e65-9b1d6a151b1d>full\_address</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7107ebf0-dc5b-11e9-b819-e3f2d5171928>houseNum</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#760da090-dc5b-11e9-b819-e3f2d5171928>street</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7bfbe070-dc5b-11e9-b819-e3f2d5171928>box</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#7ee803e0-dc5b-11e9-b819-e3f2d5171928>city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#85787730-dc5b-11e9-b819-e3f2d5171928>state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#87afc990-dc5b-11e9-b819-e3f2d5171928>zip</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c94-520d-11e7-8e65-9b1d6a151b1d>city</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9e-520d-11e7-8e65-9b1d6a151b1d>state</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c97-520d-11e7-8e65-9b1d6a151b1d>latitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c98-520d-11e7-8e65-9b1d6a151b1d>longitude</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e43ac0-520a-11e7-8e65-9b1d6a151b1d>user</a></td><td class="no-break-word">array</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe10-520a-11e7-8e65-9b1d6a151b1d>\[0\]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe1a-520a-11e7-8e65-9b1d6a151b1d>user\_id</a></td><td class="no-break-word">objectId</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe17-520a-11e7-8e65-9b1d6a151b1d>name</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"><p>Fri Sep 15 2017 17:31:32 GMT+0200 (Romance Summer Time): MongoDB Demo</p></div></td></tr><tr><td><a href=#c1e4fe19-520a-11e7-8e65-9b1d6a151b1d>type</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe1b-520a-11e7-8e65-9b1d6a151b1d>votes</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f128-2b24-11e6-b7e5-591297143e36>cool</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f129-2b24-11e6-b7e5-591297143e36>funny</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#0df0f12a-2b24-11e6-b7e5-591297143e36>useful</a></td><td class="no-break-word">numeric</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe1c-520a-11e7-8e65-9b1d6a151b1d>yelping\_since</a></td><td class="no-break-word">string</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

### <a id="70972f00-5210-11e7-8e65-9b1d6a151b1d"></a>3.2.3.1 Field **review\_id**

##### 3.2.3.1.1 **review\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_id</td></tr><tr><td>Technical name</td><td>review_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="81b90470-5210-11e7-8e65-9b1d6a151b1d"></a>3.2.3.2 Field **date**

##### 3.2.3.2.1 **date** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>date</td></tr><tr><td>Technical name</td><td>date</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="8eefbd00-5210-11e7-8e65-9b1d6a151b1d"></a>3.2.3.3 Field **stars**

##### 3.2.3.3.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Technical name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="9aadb840-5210-11e7-8e65-9b1d6a151b1d"></a>3.2.3.4 Field **type**

##### 3.2.3.4.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78ca5f0-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.5 Field **business**

##### 3.2.3.5.1 **business** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image32.png?raw=true)

##### 3.2.3.5.2 **business** Hierarchy

Parent field: **rov\_rev\_users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#b78e0580-520d-11e7-8e65-9b1d6a151b1d>\[0\]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.2.3.5.3 **business** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business</td></tr><tr><td>Technical name</td><td>business</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Unique items</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="b78e0580-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.6 Field **\[0\]**

##### 3.2.3.6.1 **\[0\]** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image33.png?raw=true)

##### 3.2.3.6.2 **\[0\]** Hierarchy

Parent field: **business**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#b78e2c92-520d-11e7-8e65-9b1d6a151b1d>business\_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c99-520d-11e7-8e65-9b1d6a151b1d>name</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9f-520d-11e7-8e65-9b1d6a151b1d>type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9b-520d-11e7-8e65-9b1d6a151b1d>open</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9d-520d-11e7-8e65-9b1d6a151b1d>stars</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9c-520d-11e7-8e65-9b1d6a151b1d>review\_count</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c95-520d-11e7-8e65-9b1d6a151b1d>full\_address</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c94-520d-11e7-8e65-9b1d6a151b1d>city</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c9e-520d-11e7-8e65-9b1d6a151b1d>state</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c97-520d-11e7-8e65-9b1d6a151b1d>latitude</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#b78e2c98-520d-11e7-8e65-9b1d6a151b1d>longitude</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.2.3.6.3 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="b78e2c92-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.7 Field **business\_id**

##### 3.2.3.7.1 **business\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>business_id</td></tr><tr><td>Technical name</td><td>business_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c99-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.8 Field **name**

##### 3.2.3.8.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c9f-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.9 Field **type**

##### 3.2.3.9.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c9b-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.10 Field **open**

##### 3.2.3.10.1 **open** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>open</td></tr><tr><td>Technical name</td><td>open</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c9d-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.11 Field **stars**

##### 3.2.3.11.1 **stars** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>stars</td></tr><tr><td>Technical name</td><td>stars</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c9c-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.12 Field **review\_count**

##### 3.2.3.12.1 **review\_count** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>review_count</td></tr><tr><td>Technical name</td><td>review_count</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c95-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.13 Field **full\_address**

##### 3.2.3.13.1 **full\_address** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>full_address</td></tr><tr><td>Technical name</td><td>full_address</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c94-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.14 Field **city**

##### 3.2.3.14.1 **city** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>city</td></tr><tr><td>Technical name</td><td>city</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c9e-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.15 Field **state**

##### 3.2.3.15.1 **state** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>state</td></tr><tr><td>Technical name</td><td>state</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c97-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.16 Field **latitude**

##### 3.2.3.16.1 **latitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>latitude</td></tr><tr><td>Technical name</td><td>latitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="b78e2c98-520d-11e7-8e65-9b1d6a151b1d"></a>3.2.3.17 Field **longitude**

##### 3.2.3.17.1 **longitude** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>longitude</td></tr><tr><td>Technical name</td><td>longitude</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c1e43ac0-520a-11e7-8e65-9b1d6a151b1d"></a>3.2.3.18 Field **user**

##### 3.2.3.18.1 **user** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image34.png?raw=true)

##### 3.2.3.18.2 **user** Hierarchy

Parent field: **rov\_rev\_users**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#c1e4fe10-520a-11e7-8e65-9b1d6a151b1d>\[0\]</a></td><td class="no-break-word">document</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.2.3.18.3 **user** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user</td></tr><tr><td>Technical name</td><td>user</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>array</td></tr><tr><td>Required</td><td>false</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Unique items</td><td>false</td></tr><tr><td>Additional items</td><td>true</td></tr></tbody></table>

### <a id="c1e4fe10-520a-11e7-8e65-9b1d6a151b1d"></a>3.2.3.19 Field **\[0\]**

##### 3.2.3.19.1 **\[0\]** Tree Diagram

![Hackolade image](/YelpChallengedatasetdocumentation_images/image35.png?raw=true)

##### 3.2.3.19.2 **\[0\]** Hierarchy

Parent field: **user**

Child field(s):

<table class="field-properties-table"><thead><tr><td>Field</td><td>Type</td><td>Req</td><td>Key</td><td>Description</td><td>Comments</td></tr></thead><tbody><tr><td><a href=#c1e4fe1a-520a-11e7-8e65-9b1d6a151b1d>user\_id</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe17-520a-11e7-8e65-9b1d6a151b1d>name</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe19-520a-11e7-8e65-9b1d6a151b1d>type</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe1b-520a-11e7-8e65-9b1d6a151b1d>votes</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr><tr><td><a href=#c1e4fe1c-520a-11e7-8e65-9b1d6a151b1d>yelping\_since</a></td><td class="no-break-word">reference</td><td>false</td><td></td><td><div class="docs-markdown"></div></td><td><div class="docs-markdown"></div></td></tr></tbody></table>

##### 3.2.3.19.3 **\[0\]** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Activated</td><td>true</td></tr><tr><td>Type</td><td>document</td></tr><tr><td>Primary key</td><td>false</td></tr><tr><td>Additional properties</td><td>false</td></tr></tbody></table>

### <a id="c1e4fe1a-520a-11e7-8e65-9b1d6a151b1d"></a>3.2.3.20 Field **user\_id**

##### 3.2.3.20.1 **user\_id** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>user_id</td></tr><tr><td>Technical name</td><td>user_id</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c1e4fe17-520a-11e7-8e65-9b1d6a151b1d"></a>3.2.3.21 Field **name**

##### 3.2.3.21.1 **name** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>name</td></tr><tr><td>Technical name</td><td>name</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c1e4fe19-520a-11e7-8e65-9b1d6a151b1d"></a>3.2.3.22 Field **type**

##### 3.2.3.22.1 **type** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>type</td></tr><tr><td>Technical name</td><td>type</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c1e4fe1b-520a-11e7-8e65-9b1d6a151b1d"></a>3.2.3.23 Field **votes**

##### 3.2.3.23.1 **votes** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>votes</td></tr><tr><td>Technical name</td><td>votes</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="c1e4fe1c-520a-11e7-8e65-9b1d6a151b1d"></a>3.2.3.24 Field **yelping\_since**

##### 3.2.3.24.1 **yelping\_since** properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>yelping_since</td></tr><tr><td>Technical name</td><td>yelping_since</td></tr><tr><td>Activated</td><td>true</td></tr><tr><td>Reference type</td><td>collectionReference</td></tr></tbody></table>

### <a id="relationships"></a>

##### 4\. Relationships

### <a id="003231f0-91f7-11e9-a924-ddc9cd9b071f"></a>4.1 Relationship **fk businesses.business\_id to checkins.business\_id**

##### 4.1.1 **fk businesses.business\_id to checkins.business\_id** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr></tbody></table>

![Hackolade image](/YelpChallengedatasetdocumentation_images/image36.png?raw=true)![Hackolade image](/YelpChallengedatasetdocumentation_images/image37.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#a080d1d0-91f6-11e9-a924-ddc9cd9b071f>checkins(1)</a></td><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f>business\_id</a></td></tr></tbody></table>

##### 4.1.2 **fk businesses.business\_id to checkins.business\_id** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk businesses.business_id to checkins.business_id</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#a080d1d0-91f6-11e9-a924-ddc9cd9b071f>checkins(1)</a></td></tr><tr><td>Child field</td><td><a href=#9c7dc021-91f6-11e9-a924-ddc9cd9b071f>business\_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="fb857d40-2b26-11e6-b7e5-591297143e36"></a>4.2 Relationship **fk\_reviewsBusinesses**

##### 4.2.1 **fk\_reviewsBusinesses** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr></tbody></table>

![Hackolade image](/YelpChallengedatasetdocumentation_images/image38.png?raw=true)![Hackolade image](/YelpChallengedatasetdocumentation_images/image39.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr></tbody></table>

##### 4.2.2 **fk\_reviewsBusinesses** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_reviewsBusinesses</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Child field</td><td><a href=#0da2aa02-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="e2514f70-2b26-11e6-b7e5-591297143e36"></a>4.3 Relationship **fk\_reviewsUsers**

##### 4.3.1 **fk\_reviewsUsers** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr></tbody></table>

![Hackolade image](/YelpChallengedatasetdocumentation_images/image40.png?raw=true)![Hackolade image](/YelpChallengedatasetdocumentation_images/image41.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr></tbody></table>

##### 4.3.2 **fk\_reviewsUsers** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_reviewsUsers</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Parent field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0da2aa00-2b24-11e6-b7e5-591297143e36>reviews</a></td></tr><tr><td>Child field</td><td><a href=#0da2aa08-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="8a3660f0-2b26-11e6-b7e5-591297143e36"></a>4.4 Relationship **fk\_tipsBusinesses**

##### 4.4.1 **fk\_tipsBusinesses** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr></tbody></table>

![Hackolade image](/YelpChallengedatasetdocumentation_images/image42.png?raw=true)![Hackolade image](/YelpChallengedatasetdocumentation_images/image43.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr></tbody></table>

##### 4.4.2 **fk\_tipsBusinesses** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_tipsBusinesses</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0dd7ead0-2b24-11e6-b7e5-591297143e36>businesses</a></td></tr><tr><td>Parent field</td><td><a href=#0dd811fc-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td></tr><tr><td>Child field</td><td><a href=#0de02832-2b24-11e6-b7e5-591297143e36>business\_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="aa956d50-2b26-11e6-b7e5-591297143e36"></a>4.5 Relationship **fk\_tipsUsers**

##### 4.5.1 **fk\_tipsUsers** Diagram

<table><thead><tr><td>Parent Table</td><td>Parent field</td></tr></thead><tbody><tr><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr></tbody></table>

![Hackolade image](/YelpChallengedatasetdocumentation_images/image44.png?raw=true)![Hackolade image](/YelpChallengedatasetdocumentation_images/image45.png?raw=true)

<table><thead><tr><td>Child Table</td><td>Child field</td></tr></thead><tbody><tr><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr></tbody></table>

##### 4.5.2 **fk\_tipsUsers** Properties

<table><thead><tr><td>Property</td><td>Value</td></tr></thead><tbody><tr><td>Name</td><td>fk_tipsUsers</td></tr><tr><td>Description</td><td></td></tr><tr><td>Parent Collection</td><td><a href=#0df0f110-2b24-11e6-b7e5-591297143e36>users</a></td></tr><tr><td>Parent field</td><td><a href=#0df0f126-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr><tr><td>Parent Cardinality</td><td>1</td></tr><tr><td>Child Collection</td><td><a href=#0de02830-2b24-11e6-b7e5-591297143e36>tips</a></td></tr><tr><td>Child field</td><td><a href=#0de02837-2b24-11e6-b7e5-591297143e36>user\_id</a></td></tr><tr><td>Child Cardinality</td><td>0..n</td></tr><tr><td>Comments</td><td></td></tr></tbody></table>

### <a id="edges"></a>