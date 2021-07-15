# OSCAL-Conversion for Security Assessment Plans
This application renders an OSCAL XML SAP (Security Assessment Plan) file to a Microsoft Word file utilizing the FedRAMP document template formats.  See https://www.fedramp.gov/templates/ for samples of these Microsoft Word templates.  Currently the application can support a valid OSCAL Release 1.0.0 OSCAL XML document for the SAP.   The application does not reference other elements that the SAP is dependent upon that exist in other layers of the OSCAL component model (Implementation layer or Controls Layer).  It only populates elements that can be mapped directly from the Assessment layer into the FedRAMP SAP template. 
# Why the project is useful
NIST is developing the Open Security Controls Assessment Language (OSCAL), a set of hierarchical, formatted, XML- and JSON-based formats that provide a standardized representation for different categories of information pertaining to the publication, implementation, and assessment of security controls. OSCAL is being developed through a collaborative approach with the public. The OSCAL website (https://csrc.nist.gov/Projects/Open-Security-Controls-Assessment-Language) provides an overview of the OSCAL project, including an XML and JSON schema reference and examples.
This minimal viable product application automates the manual mappings from OSCAL SAP to MS Word.  This application product is meant only to provide an example on how OSCAL can be converted to the target document format and is not meant to be a production application. The mappings include elements on pages in the SAP document template and maps most of the xml elements (source file) to word without any manual intervention that exists in the Assessment Plan Model.   Only XML elements that can be matched the content mappings in the included FedRAMP templates will render.
# Project Requirements
The application is coded in C# as an ASP.NET web application Visual Studio project and is meant to run in standalone mode ONLY.   This project utilizes the OpenXML (DocumentFormat.OpenXml) and the Microsoft Office Interop (Microsoft.Office.Interop.Word) namespaces to perform XML parsing and perform document rendering.
# System Software Requirements
Windows 10
Office 2016 or better
Visual Studio 2019 Community Edition

# Getting started with this project
1. Install Visual Studio 2019 Community Edition
2. Clone and checkout the Project("https://github.com/GSA/oscal-sap-to-word”)
3. Clean and Build the Project
4. Run the Project
5. Select a valid OSCAL XML SAP file and click "Upload"
6. The FedRAMP Document rendering will take several minutes to complete and will automatically be     downloaded and available after rendering is complete.   Word should open automatically once it has fully downloaded the rendered document.

# Known Issues
You may have the following error when running the code for the first time
"Could not find a part of the path '\OSCAL-Conversion\OSCAL SAP Converter\bin\roslyn\csc.exe'".
This issue can be resolved by installing the Nuget Package with Visual Studio:  Microsoft.CodeDom.Providers.DotNetComplierPlatform.NoInstall
# License Information
This project is being released under the GNU General Public License (GNU GPL) 3.0 model. Under that model there is no warranty on the open source code.   Software under the GPL may be run for all purposes, including commercial purposes and even as a tool for creating proprietary software.
# Disclaimer
This project will work with the Release 1.0.0 and some of the earlier milestone releases of the OSCAL schema from the NIST website (https://csrc.nist.gov/Projects/Open-Security-Controls-Assessment-Language) and does not address gaps between the NIST schema and the FedRAMP template requirements.   It maps elements between the two that match and will ignore those that do not.  The mappings can be adjusted and edited in Microsoft Word for the template by using the  Mapping Content Controls with the XML Panel within Microsoft Word.
# Getting help with this project
Contact the GSA FedRAMP Project Management Office for more information or support.
# Originator of Code
VITG, INC.  http://www.volpegroup.com

