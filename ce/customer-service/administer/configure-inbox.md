---
title: Configure the inbox
description: Use this article to enable and configure inbox settings in Customer Service admin center.
ms.date: 04/02/2024
author: lalexms
ms.author: laalexan
ms.reviewer:
ms.collection:
ms.topic: how-to
ms.custom: bap-template
---

# Configure the inbox

As an administrator, you can [configure the inbox setting](#configure-the-inbox-setting-for-agents) so that when your agents open Customer Service workspace or Omnichannel for Customer Service, they can select the inbox icon to show all the cases,  conversations, and records that are assigned to them. The inbox is designed to help agents efficiently work on high-velocity tasks, and promote inbox sessions to regular sessions when they need more time to resolve cases and complete their conversations.

You can configure the inbox settings for custom experiences only.

The following channels are supported in the inbox:

- Live chat
- Asynchronous chat
- Case
- Email
- Voice
- Unified routing enabled records

The following asynchronized channels are available in the conversation inbox:

- SMS
- Persistent chat
- Facebook
- WeChat
- LINE
- WhatsApp
- Teams

## Live chat and voice channel in inbox

Note the following about live conversation settings in the inbox:

- When an agent accepts a live work item, that item is then added to the relevant view in the inbox, whether or not the agent is using the inbox at the time of the live work item.
- Voice calls always open as a new session with the card added to the inbox for awareness.
- Live work item cards have a "live" visual indicator.
- Live work item unread counts accrue to the unread count on the view.

## Prerequisites

Channel providers must have **All active channels** set to **On** to use and configure the chat setting in the inbox.

## Configure the inbox setting for agents

You can configure the inbox in the Customer Service admin center by editing the agent experience profile to meet your preferred inbox settings.

1. Open the Customer Service admin center app.

1. In **Agent experience**, select **Workspaces**.

1. In **Agent experience profiles**, select **Manage**.

1. Select the profile for which you want to configure the inbox.

1. In **Inbox**, select the **Settings** icon, and then turn on the **Inbox** toggle.

1. You can either modify an existing view or create a new one by selecting **Edit**.
   The following fields can be configured:
   - **Name:** Specify a name that shows in the inbox. Alphanumeric values are valid names.
   - **Record Type:** Select the record types for which the settings need to be applied. You can select more than one record type.
   - **Chat Status**: Is available if you select the record type as chat. Select one or more of the following settings:
     -  **Assigned**
     -  **Unassigned**
     -  **Resolved**
   - **Email**: Is available if you select the record type as Email. Select all the options that you want to enable.
     - Assigned to me:
       - Emails sent to me
       - Emails assigned to me
     - Unassigned:
       - Emails in my team
       - Emails in my queue(s)
       - Emails in a shared mailbox
    - **Agent Visibility**: Select one of the following options to show or hide the view to agents:
      - **Show**
      - **Hide**

## Preconfigured inbox views

The following views are supported out of the box in the inbox:

- **Cases**: Shows all cases that the user owns, including active and resolved cases.
- **Assigned Conversations**: Shows all conversations assigned to the user, including active and closed conversations.
- **Resolved Conversations**: Shows all conversations marked as closed, and where the user was the primary agent in the conversation.
- **Unassigned Conversations**: Shows all active conversations and emails in a team or queue in which the user is a member. The user is able to assign conversations to themselves and reply to emails directly from this view.

Inbox views are refreshed every five minutes. Agents can manually refresh the view by using the **Refresh** icon.

## Configure custom views for the inbox

You can configure a customized view for the inbox so that agents can see their cases, conversations, emails, and voicemails all in a single view.

To configure multiple views for the inbox, complete the following steps.

1. Go to the agent experience profile for which you want to configure a custom view.

1. On the **Inbox** card, select **Edit**. The **Inbox** page is displayed.

1. Toggle **Enable Inbox** to **On** if it isn't already on, and then select **+ Add**. The **Add a new view** page is displayed.

1. On the **Add a new view** page, enter the following details:

   - **Name**: Type a name for the view.
   - **Agent visibility**: Select whether to **Show** or **Hide** the view from agents.
   - **Record type**: Select the records that you want to include in the multi-entity view.
  
1. For each record type, choose one of the following settings. The settings are different for each record type.

    - **Simple** opens a dropdown menu where you can choose the type of records that appears in your multi-entity view. More information: [Simple settings](#simple-settings)
       
      :::image type="content" source="../media/simple-settings-inbox.png" alt-text="Simple setting option on the Add a new view page for inbox."::: 
       
    - **Advanced** opens a **Conditions** option where you can set the desired conditions for your multi-entity view. More information: [Advanced condition builder](/business-applications-release-notes/october18/microsoft-flow/advanced-condition-builder)

      :::image type="content" source="../media/advanced-settings-inbox.png" alt-text="Advanced setting option on the Add a new view page for inbox."::: 

1. Select **Save**.

> [!NOTE]
> If you've configured new views or migrated existing views for unified routing enabled records, you might see a message that the read/unread functionality isn't supported. You can open and save the view again to ensure that the read/unread functionality is supported.

### Simple settings

The following simple settings are available out of the box for the record types.

| Record type | Simple settings |
|-----------|------------------|
| Email | - Emails sent to me <br>- Emails assigned to me <br> - Emails in my team(s) <br> - Emails in my queue(s) <br> - Emails in a shared mailbox|
| Chat | - Assigned <br> - Unassigned <br> - Resolved|
| Case | - Cases assigned to me <br> - Cases in my team(s) <br> - Case(s) in my queue(s) |
| Voicemail | - Assigned <br> - Unassigned <br> - Resolved |
| Unified Routing enabled records | - Assigned <br> - Open <br> - Closed |

## Configure custom sort in the inbox

You can configure a customized sort option for the inbox so that users can choose their desired attributes to sort by.

1. In Customer Service admin center site map, select **Workspaces**.
1. On the **Workspaces** page, next to **Agent experience profiles**, select **Manage**.
1. On the **Agent experience profiles** page, select the profile you want to edit.
1. On the **Profile** page, in **Inbox**, select **Edit**.
1. In the **Edit view** pane, in the **Sort** section, select the entity and attributes, along with sort order.

      :::image type="content" source="../media/custom-sort-inbox.png" alt-text="Custom sort option in the Edit view pane for inbox."::: 

1. Select **Save**.

## Real-time translation

For information about how to configure real-time translation for conversations in the inbox, see [Enable real-time translation of conversations](enable-real-time-translation.md).


### See also

[Create and use agent experience profiles](create-agent-experience-profile.md)<br>
[Overview of agent experience profiles](overview.md)<br>
[Use the inbox](../use/use-inbox.md)<br>
[Configure voicemail to manage inbound calls](voice-channel-voicemail.md)  
