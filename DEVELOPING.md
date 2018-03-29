Tips for Developers
===================

Extend Database
----------------
Create the custom tables USER_CAT_AFFINITY and USER_ATTR_AFFINITY and populate them with valid data, before starting off with the code customization.
Execute the following queries:
INSERT INTO KEYS VALUES((select  min(KEYS_ID)-1  from keys),'user_attr_affinity','UATTR_ID',10000,500,0,9223372036849999872,3,'0',1048576);
INSERT INTO CMDREG (STOREENT_ID, INTERFACENAME, CLASSNAME, TARGET) VALUES (0, 'com.ibm.commerce.catalog.commands.SearchDisplayCmd', 'com.ext.commerce.catalog.commands.ExtSearchDisplayCmdImpl', 'Local');
  UPDATE ATTR SET FIELD1=1;
   UPDATE ATTR SET FIELD1=0 WHERE ATTR_ID IN (SELECT ATTR_ID FROM  ATTRDESC WHERE LANGUAGE_ID=-1 AND NAME IN ('Available Sizes'));
      UPDATE ATTR SET FIELD1=0 WHERE ATTR_ID IN (SELECT ATTR_ID FROM      ATTRDESC WHERE LANGUAGE_ID=-1 AND NAME IN (Size'));
      UPDATE ATTR SET FIELD1=0 WHERE ATTR_ID IN (SELECT ATTR_ID FROM ATTRDESC WHERE LANGUAGE_ID=-1 AND NAME IN (Brand'));
      UPDATE ATTR SET FIELD1=0 WHERE ATTR_ID IN (SELECT ATTR_ID FROM ATTRDESC WHERE LANGUAGE_ID=-1 AND NAME IN ('Price'));	


Installing WCS
----------------
Follow the knowledge center link to download the media images and install WebSphere Commerce Developer instance
https://www.ibm.com/support/knowledgecenter/en/SSZLC2_8.0.0/com.ibm.commerce.install.doc/concepts/ccminstalling.htm

Publish ExtendedSites.sar by logging to WebSphere Commerce Admin Console.

 
Browsing data
--------------
Ensure that the user for whom search is to be personalized has enough orders placed across various categories and the same should be reflected in the order export from WCS. This undermines the category/brand/price/size affinity of the user and other soft-biases like color,occassion,material etc.


