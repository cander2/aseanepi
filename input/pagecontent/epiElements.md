<html>
<p>The base FHIR specification describes a set of <a href="https://hl7.org/fhir/resourcelist.html">base resources</a> used in many different use cases.</p>
<p>A FHIR profile is a customized version of a resource. It defines specific rules and constraints for how a resource should be used in a particular context (ePI in this case). This customization ensures that the data exchanged is consistent and meets the specific needs of different  organizations or systems.</p>

<p>As noted in the <a href="https://build.fhir.org/ig/cander2/aseanepi/usecases.html#recommendation">Use Cases/Recommendations section</a>, ePI Type 2 (A, B, C, and D) is recommended as the ideal approach for ASEAN markets to benefit from FHIR ePI.</p>

<p>The following content serves as a business friendly version of the recommended ePI Type 2 profile. The real ePI profile (i.e., the structured version) can be found on the Artifacts page; along with sample data.</p>
    <h3>ePI Type 2 Resources and Elements</h3>
    <h4>Bundle</h4>
    <p>The Bundle resource is a container for all resources with an ePI. There are different types of Bundle but for ePI, the Bundle type is always "Document". There can only be one Bundle per ePI.</p>
    <table style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid grey;">Bundle</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">id</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Version</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Date of last update</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Language</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Identifier</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Type</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Time Stamp</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
        </tbody>
    </table>
    <h4>Composition</h4>
    <p>The Composition resource is the basic structure for an ePI document since it carries the section headings, images, and narrrative content (e.g., text, tables, bulleted/numbered lists). There can only be one Composition per ePI Document Bundle</p>
    <table style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid grey;">Composition</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">id</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Language</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Text</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Version</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">identifier</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">status</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Type</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Subject</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Date</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Author</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Title</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Section</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">Title</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">coding</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 50px;">code system</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 50px;">code</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 50px;">display</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">text</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
        </tbody>
    </table>
    <h4>Organization</h4>
    <p>The Organization Resource describes the company name, identifier, address, and type. There must be one or more Organizations in an ePI.</p>
    <table style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid grey;">Organization</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">id</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">identifier</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Active</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Type</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Name</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">alias</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">description</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">contact</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">telecom: phone</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">telecom: email</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">telecom: url</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Address</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">use</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">type</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">text</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">line</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">City</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">state</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">postal code</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">Country</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
        </tbody>
    </table>
<h4>Regulated Authorization</h4>
<p>The Regulated Authorization resource describes a regulatory approval or licence related to a regulated medicinal product (E.g., a Market Authorization). There must be one or more Regulated Authorizations in an ePI.</p>
<head>
    <title>FHIR Resource and Data Element - Regulated Authorization</title>
</head>
    <table style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid grey;">Regulated Authorization</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">id</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">identifier</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">subject</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">type</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">description</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">region</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">status</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">statusDate</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">validityPeriod</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">indication</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">intendedUse</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">basis</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">holder</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">regulator</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
        </tbody>
    </table>
<h4>Manufactured Item Definition</h4>
<p>The Manufactured Item Definition resource describes the physical properties of the pharmaceutical dose form in its primary package (e.g., strength, ingredients, size, colour, shape). There must be one or more Manufactured Item Definitions in an ePI.</p>
<head>
    <title>FHIR Resource and Data Element - Manufactured Item Definition</title>
</head>
<body>
    <table style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid grey;">Manufactured Item Description</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">id</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">identifier</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">status</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Manufactured dose form</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">Unit of presentation</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">manufacturer</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 20px;">properties</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">colour</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">flavour</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">score</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">shape</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">surface form</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">size</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">image</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">imprint</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
            <tr>
                <td style="border: 1px solid grey; padding-left: 40px;">text</td>
                <td style="border: 1px solid grey;"></td>
            </tr>
        </tbody>
    </table>
</body>
<h4>Ingredient</h4>
<p>The Ingredient resource uniquely describes all ingredients contained in the Manufactured Item. This includes ingredient name, identifier, role (active, inactive, adjuvant), manufacturer, and strength. There must be at least one or more Ingredients in an ePI.</p>
<table style="border: 1px solid grey; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
      <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid grey;">Ingredient</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">id</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">identifier</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">status</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">for</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">role</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">allergenic indicator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">substance</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">code system</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">display</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey;">strength (Presentation - quantity)</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">presentationQuantity</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">system</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey;">strength (Presentation - ratio)</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">numerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">system</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey;">strength (Presentation - RatioRange)</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">lowNumerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">system</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">highNumerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">system</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">denominator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">system</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr style="border: 1px solid grey;">
        <td>Strength (Concentration - quantity)</td>
        <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Presentation Quantity</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey;">Strength (Concentration - ratio)</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Numerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Denominator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
<tr>
      <td style="border: 1px solid grey;">Strength (Concentration - RatioRange)</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Low Numerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">High Numerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Denominator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Basis</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; ">Reference Strength</td>
      <td style="border: 1px solid grey; "></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Substance</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">Strength</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Strength Quantity</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Strength Ratio</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">Numerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">Denominator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 40px;">Strength Ratio Range</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">Low Numerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">High Numerator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 60px;">Denominator</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Value</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Unit</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">System</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 80px;">Code</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
  </tbody>
</table>
<h4>Substance Definition</h4>
<p>The Substance Definition resource describes an ingredient in more detail (e.g., molecular weight, chemical structure). There must be one or more Substance Definitions in an ePI.</p>
<table style="border: 1px solid grey; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="border: 1px solid grey; background-color: #e0e0e0;">FHIR Resource and Data Element</th>
      <th style="border: 1px solid grey; background-color: #e0e0e0;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid grey;">Substance Definition</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">id</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">identifier</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">version</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">status</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">molecular weight</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">structure</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">name</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
    <tr>
      <td style="border: 1px solid grey; padding-left: 20px;">type</td>
      <td style="border: 1px solid grey;"></td>
    </tr>
  </tbody>
</table>
</html>