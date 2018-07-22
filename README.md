# Material Ageing ABAP Report

This report is using standard report MB5B to get material ageing based on FIFO method.
Using this report will eliminate worksheet calculations if batch is not configured on SAP ERP system

## Prequisits
User has authorization to access T-Code:MB5B
Valuation is on the plant level

## Steps to create the report
1. Create the report
    * If you have ABAPGit you can clone this project and work on it For more information follow this [link](https://blogs.sap.com/2017/06/21/abapgit-so-easy/).
    * If you have SAPLINK you can dowload this [file](https://github.com/Ibrahem-Ahmed/Material-Ageing/blob/master/NUGG_ZMM_MAGE.nugg) and install it
    * You can create it manually via T-Code: SE38 and copy includes and program
    
2. Create Status
    1. Open T-Code: SE41
    2. press Ctrl+F6 or click on Copy status icon
    3. on popup enter below parameter and click Copy
        * Frm
            * Program: SALV_DEMO_TABLE_FUNCTIONS
            * Status: SALV_STANDARD
        * to
            * Program: ZMM_MAGE
            * Status: ZSALV_STANDARD1
            
3. Assign T-code to the report via SE93


## Note
* This report is tested under SAP Netweaver 7.40 enviroment Don't know how it's going to behave on earlier versions
* It's not tested on S4Hana but it's supposed to work same as ERP 6.0 as it's built on MB5B standard report
* For complete illustration check this [SCN blog](https://blogs.sap.com/2018/07/22/inventory-ageing-abap-report/)
