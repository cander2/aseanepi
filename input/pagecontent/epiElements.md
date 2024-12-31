<html>
<p>The base FHIR specification describes a set of <a href="https://hl7.org/fhir/resourcelist.html">base resources</a> used in many different use cases.</p>
<p>A FHIR profile is a customized version of a resource. It defines specific rules and constraints for how a resource should be used in a particular context (ePI in this case). This customization ensures ßthat the data exchanged is consistent and meets the specific needs of different  organizations or systems.</p>

<p>As noted in the <a href="https://build.fhir.org/ig/cander2/aseanepi/usecases.html#recommendation">Use Cases/Recommendations section</a>, ePI Type 2 (A, B, C, and D) is recommended as the ideal approach for ASEAN markets to benefit from FHIR ePI.</p>

<p>The following content serves as a business friendly version of the recommended ePI Type 2 profile. The real ePI profile (i.e., the structured version) can be found on the Artifacts page; along with sample data.</p>
    <h3>ePI Type 2 Resources and Elements</h3>
    <h4>Bundle</h4>
    <p>The Bundle resource is a container for all resources with an ePI. There are different types of Bundle but for ePI, the Bundle type is always "Document". There can only be one Bundle per ePI.</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
            <tbody>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>id</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>System
                            generated UUID used uniquely identify this resource</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >Version</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Incremental version number for this ePI document (e.g., 1, 2, 3, 4,
                            5)</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Date of
                            last update</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Date of
                            last revision for this version of the authorized ePI document.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >Identifier</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Business
                            assigned identifier to uniquely identify this version of the ePI</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Type</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Defines
                            the type of Bundle. For ePI, the type must always be “Document”.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Time
                            Stamp</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Original
                            date of approval for this ePI. This date remains the same across all
                            versions of the ePI.</p>
                    </td>
                </tr>
            </tbody>
        </table>
    <h4>Composition</h4>
    <p>The Composition resource is the basic structure for an ePI document since it carries the section headings, images, and narrrative content (e.g., text, tables, bulleted/numbered lists). There can only be one Composition per ePI Document Bundle</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
            <tbody>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>id</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>System
                            generated UUID used uniquely identify this resource</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >Language</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            language of this ePI’s narrative text. ISO two letter language code.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Text</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Narrative
                            description of this ePI</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >Version</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Incremental version number for this Composition (e.g., 1, 2, 3, 4,
                            5)</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p><b>contained</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Images are
                            included as contained binary resources. One contained element per
                            image.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>
                        <b>Binary</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Binary
                            resource for encoded images.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 60px;">
                        <p>Id value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unique
                            identifier for this image.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 60px;">
                        <p>Content Type value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>File type
                            for the binary content (e.g., SVG, PNG, JPEG).</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 60px;">
                        <p>Data</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Actual
                            base64 encoded content for the image.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p><b>Extension</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>This
                            extension is an implementation work around to avoid unnecessary
                            validator errors, and expected to be drop in future profile releases,
                            and is used to ensure that images used in ePI sections are properly
                            referenced in the FHIR resource.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>
                        <b>Value Reference</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 60px;">
                        <p>Reference value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The use of
                            the imageReference extension avoids warning and error messages in common
                            FHIR validators.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >identifier</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unique
                            business identifier for this version of the Composition.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>status</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Status of
                            this resource (e.g., Active, retired).</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>Type</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The type
                            of ePI document template (e.g., healthcare professional, patient
                            information, instruction for use, pack label)</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>
                        <b>coding</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>        system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where document type codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Health
                            authority assigned code for this document type.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>display</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Human
                            readable text for this document type.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Subject</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Cross-reference to the Medicinal Product Definition(s) associated with
                            this ePI.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Date</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Date of
                            last revision for this version of the authorized EPI document.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Author</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Cross-reference to the Organization resource representing the Market
                            Authorization Holder</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>Title</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Simple
                            title for this ePI document.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>Section</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>    Title</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Section
                            heading defined by the market authorization holder.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>
                        <b>coding</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Section
                            heading defined by the health authority. Cannot be changed by the market
                            authorization holder</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where section heading codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Health
                            authority assigned code for this section heading.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>display</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Human
                            readable text for this section.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>
                        <b>text</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Narrative
                            text for this section (e.g., paragraphs, bulleted lists, tables).</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>Status value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The status
                            of the narrative (i.e., always “generated”).</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>        div</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Defines a
                            division or a section of the XHTML narrative.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 60px;">
                        <p>paragraph</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Paragraph
                            text</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 60px;">
                        <p>Bulleted list</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Ordered or
                            unordered bulleted list</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 60px;">
                        <p>Table</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Tables</p>
                    </td>
                </tr>
            </tbody>
        </table>
    <h4>Regulated Authorization</h4>
    <p>The Regulated Authorization resource describes a regulatory approval or licence related to a regulated medicinal product (E.g., a Market Authorization). There must be one or more Regulated Authorizations in an ePI.</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="padding-left: 20px;">id</td>
                 <td style="padding-left: 20px;">System generated UUID used uniquely identify this resource</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">identifier</td>
                 <td style="padding-left: 20px;">Business assigned unique identifier(s) for this authorization. E.g., health authority assigned market authorization or license.</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">subject</td>
                 <td style="padding-left: 20px;">Cross-reference to the Medicinal Product Definition(s) associated with this ePI.</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">type</td>
                 <td style="padding-left: 20px;">Type of authorization</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">description</td>
                 <td style="padding-left: 20px;">Narrative description of the authorization</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">region</td>
                 <td style="padding-left: 20px;">ISO two letter country code for the country in which the authorization was assigned.</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">status</td>
                 <td style="padding-left: 20px;">Status of this resource (e.g., Active, retired).</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">statusDate</td>
                 <td style="padding-left: 20px;">The date the status was assigned</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">validityPeriod</td>
                 <td style="padding-left: 20px;">Period in which the authorization is valid.</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">basis</td>
                 <td style="padding-left: 20px;">The legal/regulatory framework or reasons under which this authorization is granted.</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">holder</td>
                 <td style="padding-left: 20px;">Cross-reference to the Organization resource associated with the market authorization holder</td>
            </tr>
            <tr>
                <td style="padding-left: 20px;">regulator</td>
                 <td style="padding-left: 20px;">Cross-reference to the Organization resource associated with the regulator</td>
            </tr>
        </tbody>
    </table>           
    <h4>Organization</h4>
    <p>The Organization Resource describes the company name, identifier, address, and type. There must be one or more Organizations in an ePI.</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
            <tbody>
                <tr>
                     <td>
                        <p>id</p>
                    </td>
                     <td>
                        <p>System
                            generated UUID used uniquely identify this resource</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >identifier</p>
                    </td>
                     <td>
                        <p>Business
                            assigned unique identifier(s) for this organization. E.g., health
                            authority assigned identifier</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>Active</p>
                    </td>
                     <td>
                        <p>Whether
                            this Organization Resource is still in active use.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>Type</p>
                    </td>
                     <td>
                        <p>Type of
                            organization. E.g., marketing authorization holder, manufacturer.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>Name</p>
                    </td>
                     <td>
                        <p>Legal name
                            of the organization</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>alias</p>
                    </td>
                     <td>
                        <p
                            >Alternative name(s) for this organization. E.g., if Legal name is in
                            Thai language, the alias could be the English name.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >description</p>
                    </td>
                     <td>
                        <p>Narrative
                            description of this organization</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                                ><b>contact</b></p>
                    </td>
                     <td>
                        <p>Phone,
                            email, website details for this organization related to the ePI</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>telecom: phone</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Organization’s phone number(s) for</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>telecom: email</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Organization’s email address for</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>telecom: url</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Organization’s websites related to</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                                ><b>Address</b></p>
                    </td>
                     <td>
                        <p
                            >Organizations address</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>type</p>
                    </td>
                     <td>
                        <p>Defines
                            whether this is a mailing address (i.e., postal); or a physical address
                            that can be visited (i.e., physical); or both.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>text</p>
                    </td>
                     <td>
                        <p>Full
                            address</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>line</p>
                    </td>
                     <td>
                        <p>Street
                            name and number</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>City</p>
                    </td>
                     <td>
                        <p>City in
                            which the organization is physically located</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>state</p>
                    </td>
                     <td>
                        <p>State,
                            province, or prefecture in which the organization is physically
                            located</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>postal code</p>
                    </td>
                     <td>
                        <p>Postal
                            code for the area</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>Country</p>
                    </td>
                     <td>
                        <p>ISO two
                            letter country code for the country in which the organization is
                            located.</p>
                    </td>
                </tr>
            </tbody>
        </table>    
<h4>Medicinal Product Definition</h4>
<p>The Medicinal Product Definition resource describes regulatory details about the product (e.g., name, route of administration, legal/marketing status). There must be one or more Medicinal Product Definition.</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
            <tbody>
                <tr>
                     <td>
                        <p>id</p>
                    </td>
                     <td>
                        <p>System
                            generated UUID used uniquely identify this resource</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >identifier</p>
                    </td>
                     <td>
                        <p>Business
                            assigned unique identifier(s) for this organization. E.g., product
                            license number or market authorization number for the product.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >subject</p>
                    </td>
                     <td>
                        <p
                            >Cross-reference to the Medicinal Product Definition(s) associated with
                            this ePI.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>type</p>
                    </td>
                     <td>
                        <p>Type of
                            authorization</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >description</p>
                    </td>
                     <td>
                        <p>Narrative
                            description of what the authorization is for.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>region</p>
                    </td>
                     <td>
                        <p
                            >Jurisdiction in which the authorization was granted (i.e., ISO two
                            letter country code)</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>status</p>
                    </td>
                     <td>
                        <p>Status of
                            this resource (e.g., Active, retired).</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >statusDate</p>
                    </td>
                     <td>
                        <p>The date
                            the status was assigned</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>holder</p>
                    </td>
                     <td>
                        <p
                            >Cross-reference to the Organization Resource related to the Market
                            Authorization Holder.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                                ><b>Route</b></p>
                    </td>
                     <td>Authorized route of administration
                    </td>
                </tr>
                <tr>
                    <td>
                        <p>
                        <b>coding</b></p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where codes and display values are stored.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>code</p>
                    </td>
                     <td>
                        <p>Code for
                            the route of administration</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>display</p>
                    </td>
                     <td>
                        <p>Display
                            text for the route of administration</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >Version</p>
                    </td>
                     <td>
                        <p
                            >Incremental version number for this ePI document (e.g., 1, 2, 3, 4,
                            5)</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>Status</p>
                    </td>
                     <td>
                        <p>Status of
                            this resource (e.g., Active, retired).</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>Status
                            date</p>
                    </td>
                     <td>
                        <p>The date
                            the status was assigned</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p><b>Legal
                                Status of Supply</b></p>
                    </td>
                     <td>
                        <p>Product
                            category or product type</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 20px;">
                        <p>
                        <b>coding</b></p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where product category/type codes and display
                            values are stored.</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>code</p>
                    </td>
                     <td>
                        <p>Code for
                            the product type/category</p>
                    </td>
                </tr>
                <tr>
                    <td style="padding-left: 40px;">
                        <p>display</p>
                    </td>
                     <td>
                        <p>Display
                            text for the product type/category</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>Name</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>Product name</p>
                    </td>
                     <td>
                        <p>Full name
                            of the medicinal product</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>
                        <b>Part</b></p>
                    </td>
                     <td>
                        <p>A fragment
                            of the product name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                    <p>Part</p>
                </td>
                     <td>
                        <p>Editable
                            text for the proprietary name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                    <p>Type</p>
                </td>
                     <td>
                        Proprietary Name                  </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                    <p>coding</p>
                </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                    <p>system</p>
                </td>
                     <td>
                        <p>Reference
                            to the terminology system where codes and display values are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                    <p>code</p>
                </td>
                     <td>
                        <p>Code for
                            the proprietary name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                    <p>          display</p>
                </td>
                     <td>
                        <p>Display
                            text for the proprietary name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>
                        <b>Part</b></p>
                    </td>
                     <td>
                        <p>A fragment
                            of the product name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p>        Part</p>
                    </td>
                     <td>
                        <p>Editable
                            text for the non-proprietary name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p>Type</p>
                    </td>
                     <td>
                        <p>Non-proprietary name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p>coding</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where codes and display values are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>code</p>
                    </td>
                     <td>
                        <p>Code for
                            the Non-proprietary name part</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>display</p>
                    </td>
                     <td>
                        <p>Display
                            text for the Non-proprietary name part</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>
                        <b>Part</b></p>
                    </td>
                     <td>
                        <p>Editable
                            text for the strength part</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p>Part</p>
                    </td>
                     <td>
                        <p>Editable
                            values for the strength</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p>Type</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Strength part</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p>coding</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where codes and display values are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>          code</p>
                    </td>
                     <td>
                        <p>Code for
                            the strength part</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>          display</p>
                    </td>
                     <td>
                        <p>Display
                            text for the strength part</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>Part</b></p>
                    </td>
                     <td>
                        <p>Editable
                            text for the pharmaceutical dose form</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p>        Part</p>
                    </td>
                     <td>
                        <p>Editable
                            text for the pharmaceutical dose form</p>
                    </td>
                </tr>
                <tr>                    
                     <td style="padding-left: 40px;">
                        <p
                            >Type</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Pharmaceutical dose form</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >coding</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where codes and display values are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>code</p>
                    </td>
                     <td>
                        <p>Code for
                            the pharmaceutical dose form</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>display</p>
                    </td>
                     <td>
                        <p>Display
                            text for the pharmaceutical dose form part</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p>Usage</p>
                    </td>
                     <td>
                        <p>Country
                            and language </p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                                ><b>Country</b></p>
                    </td>
                     <td>
                        <p>Country
                            code for where this name applies</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >coding</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where country codes and display values are
                            stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >code</p>
                    </td>
                     <td>
                        <p>Code for
                            the ISO two-letter country</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >display</p>
                    </td>
                     <td>
                        <p>Display
                            name for the country</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                                ><b>language</b></p>
                    </td>
                     <td>
                        <p>Language
                            code for this name</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>coding</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where language codes and display values are
                            stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >code</p>
                    </td>
                     <td>
                        <p>ISO
                            two-letter language code</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >display</p>
                    </td>
                     <td>
                        <p>Display
                            name for the language</p>
                    </td>
                </tr>
            </tbody>
        </table>    
<h4>Manufactured Item Definition</h4>
<p>The Manufactured Item Definition resource describes the physical properties of the pharmaceutical dose form in its primary package (e.g., strength, ingredients, size, colour, shape). There must be one or more Manufactured Item Definitions in an ePI.</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
            <tbody>
                <tr>
                     <td>
                        <p>id</p>
                    </td>
                     <td>
                        <p>System
                            generated UUID used uniquely identify this resource</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >identifier</p>
                    </td>
                     <td>
                        <p>Business
                            assigned unique identifier(s) for this Manufactured Item. </p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>status</p>
                    </td>
                     <td>
                        <p>Status of
                            this resource (e.g., Active, retired).</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p><b>Manufactured dose form</b></p>
                    </td>
                     <td>
                        <p>Dose form
                            of the product in its primary packaging</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p><b>coding</b></p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where pharmaceutical dose form codes and
                            display values are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >code</p>
                    </td>
                     <td>
                        <p>Code for
                            the pharmaceutical dose form</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >display</p>
                    </td>
                     <td>
                        <p>Display
                            text for the pharmaceutical dose form</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p><b>Unit of presentation</b></p>
                    </td>
                     <td>
                        <p>Unit of
                            presentation for the product</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p><b>coding</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of presentation codes and display
                            values are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            the unit of presentation</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >display</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Display
                            text for the unit of presentation</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >manufacturer</p>
                    </td>
                     <td>
                        <p
                            >Cross-reference to the Organization resource for the manufacturer or
                            market authorization holder.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                                ><b>properties</b></p>
                    </td>
                     <td>
                        <p>Physical
                            attributes of the medicinal product</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >colour</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Colour of
                            the medicinal product</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >flavour</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Flavour of
                            the medicinal product</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >score</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Describes
                            whether the medicinal product is scored</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >shape</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Describes
                            the shape of the medicinal product</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >surface form</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Describes
                            whether the medicinal product’s surface is convex or concave</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >size</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Describes
                            the dimensions of the medicinal product</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >image</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Cross-reference to the Binary resource for the encoded version of the
                            image</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >imprint</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Describes
                            whether the medicinal product has an imprint</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >text</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Narrative
                            description of the medicinal product</p>
                    </td>
                </tr>
            </tbody>
        </table>
<h4>Ingredient</h4>
<p>The Ingredient resource uniquely describes all ingredients contained in the Manufactured Item. This includes ingredient name, identifier, role (active, inactive, adjuvant), manufacturer, and strength. There must be at least one or more Ingredients in an ePI.</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
            <tbody>
                <tr>
                     <td>
                        <p>id</p>
                    </td>
                     <td>
                        <p>System
                            generated UUID used uniquely identify this resource</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >identifier</p>
                    </td>
                     <td>
                        <p>Business
                            assigned unique identifier(s) for this ingredient. </p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>status</p>
                    </td>
                     <td>
                        <p>Status of
                            this resource (e.g., Active, retired).</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>for</p>
                    </td>
                     <td>
                        <p
                            >Cross-reference to the Manufactured Item this ingredient is associated
                            with.</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>role</p>
                    </td>
                     <td>
                        <p>Whether
                            the ingredient is active or inactive</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>allergenic
                            indicator</p>
                    </td>
                     <td>
                        <p>Flags if
                            the ingredient is a known allergen</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                                ><b>substance</b></p>
                    </td>
                     <td>
                        <p>The
                            substance that comprises this ingredient</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system substance codes and display values are
                            stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this substance.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >display</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Human
                            readable text for this substance.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strength (Presentation - quantity)</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            presentation quantity of the substance expressed per unit of
                            presentation</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >presentationQuantity</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >value</p>
                    </td>
                     <td>
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >unit</p>
                    </td>
                     <td>
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >code</p>
                    </td>
                     <td>
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strength (Presentation - ratio)</b></p>
                    </td>
                     <td>
                        <p>The
                            presentation quantity of the substance expressed as a ratio</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >numerator</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td>
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td>
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td>
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >denominator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td>
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strength (Presentation - RatioRange)</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            presentation quantity of the substance expressed as a range</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >lowNumerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >highNumerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >denominator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strength (Concentration - quantity)</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            concentration<b></b>quantity of the substance expressed per unit of
                            presentation</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >presentationQuantity</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strength (Concentration - ratio)</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            concentration<b></b>quantity of the substance expressed as a ratio</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >numerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >denominator</p>
                    </td>
                     <td style="padding-left: 60px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 0px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strength (Concentration - RatioRange)</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            concentration<b></b>quantity of the substance expressed as a range</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >lowNumerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >highNumerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >denominator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p>basis</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td>
                        <p
                            >referenceStrength</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Describes
                            moiety as the quantity of substance.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >substance</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Cross-reference to the substance identifier</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >strength</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Quantity
                            of substance</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strengthQuanitity</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            quantity of the substance expressed per unit of measure.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strengthRatio</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            quantity of the substance expressed as a ratio.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >numerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >denominator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                                ><b>strengthRatioRange</b></p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>The
                            quantity of the substance expressed as a range.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >lowNumerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >highNumerator</p>
                    </td>
                     <td style="padding-left: 20px;">
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td>
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td>
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td>
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 40px;">
                        <p
                            >denominator</p>
                    </td>
                     <td>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >value</p>
                    </td>
                     <td>
                        <p>Numeric
                            quantity </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >unit</p>
                    </td>
                     <td>
                        <p>Unit of
                            measure</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >system</p>
                    </td>
                     <td>
                        <p>Reference
                            to the terminology system where unit of measure codes and display values
                            are stored.</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 60px;">
                        <p
                            >code</p>
                    </td>
                     <td>
                        <p>Code for
                            this unit</p>
                    </td>
                </tr>
            </tbody>
        </table>


<h4>Substance Definition</h4>
<p>The Substance Definition resource describes an ingredient in more detail (e.g., molecular weight, chemical structure). There must be one or more Substance Definitions in an ePI.</p>
    <table border="1" style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
            <tbody>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>id</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>System
                            generated UUID used uniquely identify this resource</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >identifier</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Business
                            assigned unique identifier(s) for this substance. </p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p
                            >version</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p
                            >Incremental version number for this ePI document (e.g., 1, 2, 3, 4,
                            5)</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>status</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Status of
                            this resource (e.g., Active, retired).</p>
                    </td>
                </tr>
                <tr>
                     <td style="padding-left: 20px;">
                        <p>name</p>
                    </td>
                     <td style="padding-left: 20px;">
                        <p>Human
                            readable name for this substance.</p>
                    </td>
                </tr>
            </tbody>
        </table>
</html>