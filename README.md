# HDG_PowerApps-Canvas-Samples

## Custom notification

![Custom notification](img/CustomNotiPowerApps.png)

### Custom property

(Input)
1. AlertMesssage - text : Message to display notification
2. NotificationType - text : Notification type. Select Enter one of the NotificationTypes. (ex : CustomNotificatoin_HDG.Notification.Success)
3. NotificationWidth - number : Set notification width
4. FontSize - number : Set Notification font size
5. Duration - number : Set Notification duration (ms)
6. InsertNotification - boolean : If change this property, the notification list is inserted
7. FillColor - record : Color record. If you want to change color of each type, check here.
- Default value
{
    Success: ColorValue("#28a745"),
    Warning: ColorValue("#ffc107"),
    Error: ColorValue("#dc3545"),
    Info: ColorValue("#17a2b8")
}
8. NotificationTypes - record : Notification type record.
- Default value
{
  Success: "Success",
  Warning: "Warning",
  Error: "Error",
  Info: "Info"
}
9. Icons - record : Icon record. If you want to change Icon of each type, check here.
-Default value
{
    Success: "data:image/svg+xml;utf8, %3Csvg%20%20viewBox%3D%270%200%202048%202048%27%20xmlns%3D%27http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%27%3E%3Cpath%20d%3D%27M1491%20595l90%2090-749%20749-365-365%2090-90%20275%20275%20659-659zM1024%200q141%200%20272%2036t245%20103%20207%20160%20160%20208%20103%20245%2037%20272q0%20141-36%20272t-103%20245-160%20207-208%20160-245%20103-272%2037q-141%200-272-36t-245-103-207-160-160-208-103-244-37-273q0-141%2036-272t103-245%20160-207%20208-160T751%2037t273-37zm0%201920q123%200%20237-32t214-90%20182-141%20140-181%2091-214%2032-238q0-123-32-237t-90-214-141-182-181-140-214-91-238-32q-123%200-237%2032t-214%2090-182%20141-140%20181-91%20214-32%20238q0%20123%2032%20237t90%20214%20141%20182%20181%20140%20214%2091%20238%2032z%27%20fill%3D%27%23FFFFFF%27%3E%3C%2Fpath%3E%3C%2Fsvg%3E",
    
    Warning: "data:image/svg+xml;utf8, %3Csvg%20%20viewBox%3D%270%200%202048%202048%27%20xmlns%3D%27http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%27%3E%3Cpath%20d%3D%27M960%200q133%200%20255%2034t230%2096%20194%20150%20150%20195%2097%20229%2034%20256q0%20133-34%20255t-96%20230-150%20194-195%20150-229%2097-256%2034q-133%200-255-34t-230-96-194-150-150-195-97-229T0%20960q0-133%2034-255t96-230%20150-194%20195-150%20229-97T960%200zm0%201792q114%200%20220-30t199-84%20169-130%20130-168%2084-199%2030-221q0-114-30-220t-84-199-130-169-168-130-199-84-221-30q-115%200-221%2030t-198%2084-169%20130-130%20168-84%20199-30%20221q0%20114%2030%20220t84%20199%20130%20169%20168%20130%20199%2084%20221%2030zM896%20512h128v640H896V512zm0%20768h128v128H896v-128z%27%20fill%3D%27%23FFFFFF%27%3E%3C%2Fpath%3E%3C%2Fsvg%3E",
    
    Error: "data:image/svg+xml;utf8, %3Csvg%20%20viewBox%3D%270%200%202048%202048%27%20xmlns%3D%27http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%27%3E%3Cpath%20d%3D%27M1024%200q141%200%20272%2036t244%20104%20207%20160%20161%20207%20103%20245%2037%20272q0%20141-36%20272t-104%20244-160%20207-207%20161-245%20103-272%2037q-141%200-272-36t-244-104-207-160-161-207-103-245-37-272q0-141%2036-272t104-244%20160-207%20207-161T752%2037t272-37zm0%201920q124%200%20238-32t214-90%20181-140%20140-181%2091-214%2032-239q0-124-32-238t-90-214-140-181-181-140-214-91-239-32q-124%200-238%2032t-214%2090-181%20140-140%20181-91%20214-32%20239q0%20124%2032%20238t90%20214%20140%20181%20181%20140%20214%2091%20239%2032zm443-1249l-352%20353%20352%20353-90%2090-353-352-353%20352-90-90%20352-353-352-353%2090-90%20353%20352%20353-352%2090%2090z%27%20fill%3D%27%23FFFFFF%27%3E%3C%2Fpath%3E%3C%2Fsvg%3E",
    
    Info: "data:image/svg+xml;utf8, %3Csvg%20%20viewBox%3D%270%200%202048%202048%27%20xmlns%3D%27http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%27%3E%3Cpath%20d%3D%27M960%201920q-133%200-255-34t-230-96-194-150-150-195-97-229T0%20960q0-133%2034-255t96-230%20150-194%20195-150%20229-97T960%200q133%200%20255%2034t230%2096%20194%20150%20150%20195%2097%20229%2034%20256q0%20133-34%20255t-96%20230-150%20194-195%20150-229%2097-256%2034zm0-1792q-115%200-221%2030t-198%2084-169%20130-130%20168-84%20199-30%20221q0%20114%2030%20220t84%20199%20130%20169%20168%20130%20199%2084%20221%2030q114%200%20220-30t199-84%20169-130%20130-168%2084-199%2030-221q0-114-30-220t-84-199-130-169-168-130-199-84-221-30zm-64%20640h128v640H896V768zm0-256h128v128H896V512z%27%20fill%3D%27%23FFFFFF%27%3E%3C%2Fpath%3E%3C%2Fsvg%3E"
}

(Output)
1. NotificationHeight - number : Set notification height. Default value is (Notification count) * 109

If you want to make notification, make button and set to OnSelect like below code.

<pre>
    <code>
        Set(varNotificationMessage, txtMessage.Text); Set(varNotificationType, Component1_1.NotificationTypes.Info); Set(varNotification, !varNotification);
    </code>
</pre>

And set variable on component like below.
- AlertMessage : varNotificationMessage
- InsertNotification : varNotification
- NotificationType : varNotificationType
