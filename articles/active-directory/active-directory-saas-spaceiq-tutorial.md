---
title: 'Tutorial: Azure Active Directory integration with SpaceIQ | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and SpaceIQ.
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman
ms.reviewer: joflore

ms.assetid: 5b55ae29-491f-401f-9299-d3a6b64a1b99
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 09/04/2017
ms.author: jeedes

---
# Tutorial: Azure Active Directory integration with SpaceIQ

In this tutorial, you learn how to integrate SpaceIQ with Azure Active Directory (Azure AD).

Integrating SpaceIQ with Azure AD provides you with the following benefits:

- You can control in Azure AD who has access to SpaceIQ.
- You can enable your users to automatically get signed-on to SpaceIQ (Single Sign-On) with their Azure AD accounts.
- You can manage your accounts in one central location - the Azure portal.

If you want to know more details about SaaS app integration with Azure AD, see [what is application access and single sign-on with Azure Active Directory](manage-apps/what-is-single-sign-on.md).

## Prerequisites

To configure Azure AD integration with SpaceIQ, you need the following items:

- An Azure AD subscription
- A SpaceIQ single sign-on enabled subscription

> [!NOTE]
> To test the steps in this tutorial, we do not recommend using a production environment.

To test the steps in this tutorial, you should follow these recommendations:

- Do not use your production environment, unless it is necessary.
- If you don't have an Azure AD trial environment, you can [get a one-month trial](https://azure.microsoft.com/pricing/free-trial/).

## Scenario description
In this tutorial, you test Azure AD single sign-on in a test environment. 
The scenario outlined in this tutorial consists of two main building blocks:

1. Adding SpaceIQ from the gallery
2. Configuring and testing Azure AD single sign-on

## Adding SpaceIQ from the gallery
To configure the integration of SpaceIQ into Azure AD, you need to add SpaceIQ from the gallery to your list of managed SaaS apps.

**To add SpaceIQ from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon. 

	![The Azure Active Directory button][1]

2. Navigate to **Enterprise applications**. Then go to **All applications**.

	![The Enterprise applications blade][2]
	
3. To add new application, click **New application** button on the top of dialog.

	![The New application button][3]

4. In the search box, type **SpaceIQ**, select **SpaceIQ** from result panel then click **Add** button to add the application.

	![SpaceIQ in the results list](./media/active-directory-saas-spaceiq-tutorial/tutorial_spaceiq_addfromgallery.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with SpaceIQ based on a test user called "Britta Simon."

For single sign-on to work, Azure AD needs to know what the counterpart user in SpaceIQ is to a user in Azure AD. In other words, a link relationship between an Azure AD user and the related user in SpaceIQ needs to be established.

In SpaceIQ, assign the value of the **user name** in Azure AD as the value of the **Username** to establish the link relationship.

To configure and test Azure AD single sign-on with SpaceIQ, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
3. **[Create a SpaceIQ test user](#create-a-spaceiq-test-user)** - to have a counterpart of Britta Simon in SpaceIQ that is linked to the Azure AD representation of user.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal and configure single sign-on in your SpaceIQ application.

**To configure Azure AD single sign-on with SpaceIQ, perform the following steps:**

1. In the Azure portal, on the **SpaceIQ** application integration page, click **Single sign-on**.

	![Configure single sign-on link][4]

2. On the **Single sign-on** dialog, select **Mode** as	**SAML-based Sign-on** to enable single sign-on.
 
	![Single sign-on dialog box](./media/active-directory-saas-spaceiq-tutorial/tutorial_spaceiq_samlbase.png)

3. On the **SpaceIQ Domain and URLs** section, perform the following steps:

	![SpaceIQ Domain and URLs single sign-on information](./media/active-directory-saas-spaceiq-tutorial/tutorial_spaceiq_url.png)

    a. In the **Identifier** textbox, type the URL: `https://api.spaceiq.com`

	b. In the **Reply URL** textbox, type a URL using the following pattern: `https://api.spaceiq.com/saml/<instanceid>/callback`

	> [!NOTE] 
	> Update these values with the actual Reply URL and identifier which is explained later in the tutorial.
 
4. On the **SAML Signing Certificate** section, click **(Certificate Base64)** and then save the certificate file on your computer.

	![The Certificate download link](./media/active-directory-saas-spaceiq-tutorial/tutorial_spaceiq_certificate.png) 

5. Click **Save** button.

	![Configure Single Sign-On Save button](./media/active-directory-saas-spaceiq-tutorial/tutorial_general_400.png)

6. On the **SpaceIQ Configuration** section, click **Configure SpaceIQ** to open **Configure sign-on** window. Copy the **SAML Entity ID** from the **Quick Reference section.**

	![SpaceIQ Configuration](./media/active-directory-saas-spaceiq-tutorial/tutorial_spaceiq_configure.png) 

7.  Open a new browser window, and then sign in to your SpaceIQ environment as an administrator.

8. Once you are logged in, click on the puzzle sign at the top right, then click on **"Integrations"**

	![Account settings](./media/active-directory-saas-spaceiq-tutorial/setting1.png) 

9. Under **All PROVISIONING & SSO**, click on the **Azure** tile to add an instance of Azure as IDP.

	![SAML icon](./media/active-directory-saas-spaceiq-tutorial/setting2.png)

10. In the **SSO** dialog box, perform the following steps:

    ![SAML Authentication Settings](./media/active-directory-saas-spaceiq-tutorial/setting3.png)

	a. In the **SAML Issuer URL** box, paste the **SAML Entity ID** value copied from the Azure AD application configuration window.
	
	b. Copy the **SAML CallBack Endpoint URL (read-only)** value and paste the value in the **Reply URL** box in the Azure portal, under SpaceIQ **Domain and URLs** section.
	
	c. Copy the **SAML Audience URI (read-only)** value and paste the value in the **Identifier** box in the Azure portal, under SpaceIQ **Domain and URLs** section.

	d. Open the downloaded certificate file in notepad, copy the content, and then paste it in the **X.509 Certificate** box.
	
	e. Click **Save**.

> [!TIP]
> You can now read a concise version of these instructions inside the [Azure portal](https://portal.azure.com), while you are setting up the app!  After adding this app from the **Active Directory > Enterprise Applications** section, simply click the **Single Sign-On** tab and access the embedded documentation through the **Configuration** section at the bottom. You can read more about the embedded documentation feature here: [Azure AD embedded documentation]( https://go.microsoft.com/fwlink/?linkid=845985)

### Create an Azure AD test user

The objective of this section is to create a test user in the Azure portal called Britta Simon.

   ![Create an Azure AD test user][100]

**To create a test user in Azure AD, perform the following steps:**

1. In the Azure portal, in the left pane, click the **Azure Active Directory** button.

    ![The Azure Active Directory button](./media/active-directory-saas-spaceiq-tutorial/create_aaduser_01.png)

2. To display the list of users, go to **Users and groups**, and then click **All users**.

    ![The "Users and groups" and "All users" links](./media/active-directory-saas-spaceiq-tutorial/create_aaduser_02.png)

3. To open the **User** dialog box, click **Add** at the top of the **All Users** dialog box.

    ![The Add button](./media/active-directory-saas-spaceiq-tutorial/create_aaduser_03.png)

4. In the **User** dialog box, perform the following steps:

    ![The User dialog box](./media/active-directory-saas-spaceiq-tutorial/create_aaduser_04.png)

    a. In the **Name** box, type **BrittaSimon**.

    b. In the **User name** box, type the email address of user Britta Simon.

    c. Select the **Show Password** check box, and then write down the value that's displayed in the **Password** box.

    d. Click **Create**.
  
### Create a SpaceIQ test user

In this section, you create a user called Britta Simon in SpaceIQ. Work [SpaceIQ support team](mailto:eng@spaceiq.com) to add the users in the SpaceIQ platform. Users must be created and activated before you use single sign-on.

### Assign the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to SpaceIQ.

![Assign the user role][200] 

**To assign Britta Simon to SpaceIQ, perform the following steps:**

1. In the Azure portal, open the applications view, and then navigate to the directory view and go to **Enterprise applications** then click **All applications**.

	![Assign User][201] 

2. In the applications list, select **SpaceIQ**.

	![The SpaceIQ link in the Applications list](./media/active-directory-saas-spaceiq-tutorial/tutorial_spaceiq_app.png)  

3. In the menu on the left, click **Users and groups**.

	![The "Users and groups" link][202]

4. Click **Add** button. Then select **Users and groups** on **Add Assignment** dialog.

	![The Add Assignment pane][203]

5. On **Users and groups** dialog, select **Britta Simon** in the Users list.

6. Click **Select** button on **Users and groups** dialog.

7. Click **Assign** button on **Add Assignment** dialog.
	
### Test single sign-on

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

When you click the SpaceIQ tile in the Access Panel, you should get automatically signed-on to your SpaceIQ application.
For more information about the Access Panel, see [Introduction to the Access Panel](active-directory-saas-access-panel-introduction.md). 

## Additional resources

* [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](active-directory-saas-tutorial-list.md)
* [What is application access and single sign-on with Azure Active Directory?](manage-apps/what-is-single-sign-on.md)



<!--Image references-->

[1]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_04.png

[100]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_201.png
[202]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_202.png
[203]: ./media/active-directory-saas-spaceiq-tutorial/tutorial_general_203.png

