### Purpose
To define a common standard for exchanging electronic medicinal product information (ePI) in ASEAN.

We support the following:
- Common metadata resources
- National HCP template (No exist)
- National PIL template
- Optional ASEAN SmPC template for HCP
- Optional ASEAN PIL template


### Goals
The immediate goal of this specification is to expose ePI consumers and the vendor community to a set of profiles that identify the data elements, code systems and value sets commonly used in ePIs regardless of the jurisdiction.

The strategic goal is to offer a better route for patients to access trustworthy, up-to-date medicinal product information that better meets their individual needs.

### Scope

#### In Scope
- ASEAN Countries
- ePI (information for healthcare practitioner, information for the patient, package label). Human pharmaceutical, radiopharmaceutical and biologic medicinal products (prescription and physician-administered).
<head>
    <title>Two-Column Bulleted List</title>
    <style>
        .two-column-list {
            display: grid;
            grid-template-columns: 2fr 2fr;
            list-style-type: circle;
            padding: 2;
        }
        .two-column-list li {
            margin-bottom: 0.5em;
        }
    </style>
</head>
<body>
<ul>
  <li>
    <p>HL7 FHIR resources:</p>
    <ul class="two-column-list">
        <li>List</li>
        <li>Manufactured Item Definition</li>
        <li>Bundle</li>
        <li>Administrable Product Definition</li>
        <li>Composition </li>
        <li>Ingredient</li>
        <li>Binary</li>
        <li>Substance Definition</li>
        <li>Organization</li>
        <li>Packaged Product Definition</li>
        <li>Regulated Authorization</li>
        <li>Clinical Use Definition</li>
        <li>Medicinal Product Definition</li>
        <li>Medication Statement</li>
    </ul>
  </li>
</ul>

</body>

#### Out of Scope
Over the counter (non-prescription) drugs, Investigational and authorized medicinal products, Medical devices co-packed with a biopharmaceutical product (e.g., pre-filled syringe), natural health products, medical devices, food and veterinary drugs.

### Background

In recent years, e-labeling has been introduced in many countries around the world, including the ASEAN countries. As of November 2024, 3 ASEAN countries - Singapore, Malaysia, and Thailand - have issued official e-labeling guidance, while Indonesia initiated a nation-wide e-labeling pilot in June 2023. Current e-labeling initiatives in ASEAN focus on publishing electronic labels in PDF format online, integrating machine-readable codes on packaging for accessibility, and phasing out paper labels. This transition has demonstrated significant benefits, providing patients and healthcare professionals with timely, accessible product information, while also promoting resource efficiency and environmental sustainability by reducing paper usage.

However, to fully leverage e-labeling’s potential, integrate it with other healthcare systems and maximise the benefits for patients’ health, there is a need to transition from the conventional PDF format of e-label to a structured-content format complying with international standards. HL7 FHIR is a widely used standard in ASEAN healthcare systems, making it an ideal choice to adopt for structured e-label. Internationally, the EMA and Jordan have issued regulations to transition to FHIR-based electronic product information (ePI) format, sparking interest among ASEAN regulators. Notably, Thailand and Malaysia have already initiated conversation on how to move forward in this direction.

Firstly, an important aspect needed to be considered for the transition from unstructured content to FHIR is the current labeling template in ASEAN countries. At present, there is no harmonized single regional template that have been adopted for both healthcare professional and patient labels in ASEAN. Some countries such as Thailand, Malaysia, Indonesia require national template for the patient information leaflet (PIL), though these templates differ across countries (see APPENDIX 1). In terms of the healthcare professional labels, Thailand has started to mandate the ASEAN template for newly registered products and will also require the template to be used during renewal and labeling variations, while all other countries haven’t enforced a national template. The absence of national and regional template poses a challenge in transitioning towards FHIR standard, as an established template would facilitate semi-automated conversion, simplify the development of FHIR authoring tool as well as provide a uniform e-label structure.

The ASEAN template for both healthcare professional labeling and patient labeling was agreed upon among ASEAN countries in 2003; however, it has not been officially adopted by most countries (except for Thailand) (see APPENDIX 2). Utilising this template in each country as part of the FHIR transition - beginning with products for which paper labels have been eliminated – would facilitate the establishing of FHIR ePI structure and transition in each country as well as avoiding supply challenge for products still using paper labels. A common format would also allow ASEAN countries to exchange experience, technical expertise and accelerate the FHIR adoption process, bringing along the benefits to patients through FHIR application use cases at the earliest.

Another critical aspect to consider in the transition to FHIR-based e-PI is the establishment of controlled terminology within each country. Controlled terminology refers to standardized vocabularies to ensure consistent and accurate representation of data within FHIR. Currently, no ASEAN country has specific requirements for the use of standard terminology in e-labeling. This poses a challenge for conversion to FHIR e-PI, ensuring consistency and interoperability, particularly as FHIR-based e-labels are integrated with other healthcare systems.

The specific controlled terminologies required for FHIR ePI implementation vary depending on the type of ePI being adopted (Type 1, 2, or 3). Particularly for type 2 ePI, terminologies for specific elements like dosage form and ingredients need to be standardized (please see section for more details). To address this gap, it is recommended that each ASEAN country consider to adopt internationally recognized standards, such as ISO IDMP (Identification of Medicinal Products), to establish robust and consistent terminologies. Leveraging such standards will facilitate alignment with global best practices, support automated processes, and enhance the integration of e-labels into digital healthcare ecosystems.
