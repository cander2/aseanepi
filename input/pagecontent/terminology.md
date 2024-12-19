<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>Controlled Terminology</title>
</head>
<body>
    <h1>Controlled Terminology</h1>
    <p>Controlled terminology is a key part of FHIR since it provides a consistent and standardized method for naming identified terms.</p>
    <p>Each Resource contains a set of elements and attributes. Some elements are bound to a controlled terminology. The bindings offer various degrees of flexibility:</p>
    <ul>
        <li><b>Required</b>: Required to comply with this specific set of terms.</li>
        <li><b>Extensible</b>: Required to comply with this specific set of terms but additional terms can be added.</li>
        <li><b>Preferred</b>: Not required but encouraged to use these terms to facilitate international harmonization.</li>
        <li><b>Example</b>: Not required. Terms are optional and only presented as an example.</li>
    </ul>
    <p>The following is a list of controlled terminologies that are preferred because they support international harmonization. Refer to Appendix XX for a complete list in-scope elements and their corresponding terminologies.</p>
    <table style="border: 1px solid grey; border-collapse: collapse;">
        <thead>
            <tr>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Topic</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Type of standard</th>
                <th style="border: 1px solid grey; background-color: #e0e0e0;">Preferred Standard</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="border: 1px solid grey;">Language</td>
                <td style="border: 1px solid grey;">International</td>
                <td style="border: 1px solid grey;">ISO 639-1 (Two letter)</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Country code</td>
                <td style="border: 1px solid grey;">International</td>
                <td style="border: 1px solid grey;">ISO 3166-1 alpha-2 (Two letter)</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Pack Type</td>
                <td style="border: 1px solid grey;">EU</td>
                <td style="border: 1px solid grey;">EDQM Standard Terms</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Pack Material</td>
                <td style="border: 1px solid grey;">EU</td>
                <td style="border: 1px solid grey;">EDQM Standard Terms</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Route of administration</td>
                <td style="border: 1px solid grey;">EU</td>
                <td style="border: 1px solid grey;">EDQM Standard Terms</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Pharmaceutical dose form</td>
                <td style="border: 1px solid grey;">EU</td>
                <td style="border: 1px solid grey;">EDQM Standard Terms</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Combined Pharmaceutical dose form</td>
                <td style="border: 1px solid grey;">EU</td>
                <td style="border: 1px solid grey;">EDQM Standard Terms</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Unit of presentation</td>
                <td style="border: 1px solid grey;">EU</td>
                <td style="border: 1px solid grey;">EDQM Standard Terms</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Units of Measure</td>
                <td style="border: 1px solid grey;">International</td>
                <td style="border: 1px solid grey;">EDQM Standard Terms</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Substance code</td>
                <td style="border: 1px solid grey;">US</td>
                <td style="border: 1px solid grey;">FDA’s UNII (from Global Substance Registration System (G-SRS))</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Substance name</td>
                <td style="border: 1px solid grey;">International</td>
                <td style="border: 1px solid grey;">WHO INN</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Colour</td>
                <td style="border: 1px solid grey;">US</td>
                <td style="border: 1px solid grey;">FDA SPL Resources</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Shape</td>
                <td style="border: 1px solid grey;">US</td>
                <td style="border: 1px solid grey;">FDA SPL Resources</td>
            </tr>
            <tr>
                <td style="border: 1px solid grey;">Flavour</td>
                <td style="border: 1px solid grey;">US</td>
                <td style="border: 1px solid grey;">FDA SPL Resources</td>
            </tr>
        </tbody>
    </table>
</body>
</html>