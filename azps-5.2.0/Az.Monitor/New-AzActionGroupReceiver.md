---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391299"
---
# <span data-ttu-id="85501-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="85501-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85501-102">SYNOPSIS</span></span>
<span data-ttu-id="85501-103">Skapar en ny mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="85501-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="85501-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85501-104">SYNTAX</span></span>

### <span data-ttu-id="85501-105">NewEmailReceiver (standard)</span><span class="sxs-lookup"><span data-stu-id="85501-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85501-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85501-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85501-115">DESCRIPTION</span></span>
<span data-ttu-id="85501-116">Cmdleten **New-AzActionGroupReceiver** skapar en ny grupp mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="85501-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="85501-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85501-117">EXAMPLES</span></span>

### <span data-ttu-id="85501-118">Exempel 1: skapa en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="85501-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="85501-119">Det här kommandot skapar en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="85501-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="85501-120">Exempel 2: skapa en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="85501-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="85501-121">Det här kommandot skapar en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="85501-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="85501-122">Exempel 3: skapa en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="85501-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="85501-123">Det här kommandot skapar en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="85501-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="85501-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85501-124">PARAMETERS</span></span>

### <span data-ttu-id="85501-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="85501-126">Skapa en ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="85501-127">-AutomationAccountId</span></span>
<span data-ttu-id="85501-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="85501-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="85501-130">Skapa en AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="85501-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="85501-132">URI: n där webhookarna ska skickas</span><span class="sxs-lookup"><span data-stu-id="85501-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="85501-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="85501-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="85501-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="85501-136">Skapa en AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="85501-138">Skapa en ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="85501-139">-CallbackUrl</span></span>
<span data-ttu-id="85501-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="85501-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="85501-141">-ConnectionId</span></span>
<span data-ttu-id="85501-142">ITSM anslutnings-ID för denna mottagare</span><span class="sxs-lookup"><span data-stu-id="85501-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="85501-143">-CountryCode</span></span>
<span data-ttu-id="85501-144">Anger lands koden för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="85501-144">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85501-145">-DefaultProfile</span></span>
<span data-ttu-id="85501-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="85501-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85501-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="85501-147">-EmailAddress</span></span>
<span data-ttu-id="85501-148">Anger adressen för e-postmottagaren.</span><span class="sxs-lookup"><span data-stu-id="85501-148">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-149">-EmailReceiver</span></span>
<span data-ttu-id="85501-150">Anger att du vill skapa en e-postmottagare</span><span class="sxs-lookup"><span data-stu-id="85501-150">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="85501-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="85501-152">programmet resourceId för funktioner</span><span class="sxs-lookup"><span data-stu-id="85501-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="85501-153">-FunctionName</span></span>
<span data-ttu-id="85501-154">functionName</span><span class="sxs-lookup"><span data-stu-id="85501-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="85501-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="85501-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="85501-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="85501-157">-IdentifierUri</span></span>
<span data-ttu-id="85501-158">ID för identitets-URI för AAD auth</span><span class="sxs-lookup"><span data-stu-id="85501-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="85501-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="85501-160">visar om den här instansen är en global Runbook</span><span class="sxs-lookup"><span data-stu-id="85501-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-161">-ItsmReceiver</span></span>
<span data-ttu-id="85501-162">Skapa en ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-163">-LogicAppReceiver</span></span>
<span data-ttu-id="85501-164">Skapa en LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-165">-Namn</span><span class="sxs-lookup"><span data-stu-id="85501-165">-Name</span></span>
<span data-ttu-id="85501-166">Anger namnet på mottagaren.</span><span class="sxs-lookup"><span data-stu-id="85501-166">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="85501-167">-ObjectId</span></span>
<span data-ttu-id="85501-168">webhook-programobjekt-ID för AAD auth</span><span class="sxs-lookup"><span data-stu-id="85501-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-169">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="85501-169">-PhoneNumber</span></span>
<span data-ttu-id="85501-170">Anger telefonnumret för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="85501-170">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-171">-Region</span><span class="sxs-lookup"><span data-stu-id="85501-171">-Region</span></span>
<span data-ttu-id="85501-172">ITSM region för denna mottagare</span><span class="sxs-lookup"><span data-stu-id="85501-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85501-173">-ResourceId</span></span>
<span data-ttu-id="85501-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="85501-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="85501-175">-RoleId</span></span>
<span data-ttu-id="85501-176">Mottagarens roll-ID</span><span class="sxs-lookup"><span data-stu-id="85501-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="85501-177">-RunbookName</span></span>
<span data-ttu-id="85501-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="85501-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="85501-179">-ServiceUri</span></span>
<span data-ttu-id="85501-180">Anger URI för webhook-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="85501-180">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-181">-SmsReceiver</span></span>
<span data-ttu-id="85501-182">Anger att SMS-mottagare ska skapas</span><span class="sxs-lookup"><span data-stu-id="85501-182">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="85501-183">-TenantId</span></span>
<span data-ttu-id="85501-184">klient-ID för AAD auth</span><span class="sxs-lookup"><span data-stu-id="85501-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="85501-185">-TicketConfiguration</span></span>
<span data-ttu-id="85501-186">ITSM TicketConfiguration för denna mottagare</span><span class="sxs-lookup"><span data-stu-id="85501-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="85501-187">-UseAadAuth</span></span>
<span data-ttu-id="85501-188">flaggan för att lägga till auth</span><span class="sxs-lookup"><span data-stu-id="85501-188">the flag to use add auth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="85501-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="85501-190">Flaggan som används för att använda vanligt aviserings schema.</span><span class="sxs-lookup"><span data-stu-id="85501-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="85501-191">Det här värdet kommer att vara neglectedfor SMS, Azure App push, ITSM och Voice recievers.</span><span class="sxs-lookup"><span data-stu-id="85501-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="85501-192">-VoiceCountryCode</span></span>
<span data-ttu-id="85501-193">Land koden för röst mottagaren</span><span class="sxs-lookup"><span data-stu-id="85501-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="85501-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="85501-195">Telefonnumret till röst mottagaren</span><span class="sxs-lookup"><span data-stu-id="85501-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-196">-VoiceReceiver</span></span>
<span data-ttu-id="85501-197">Skapa en röst mottagare</span><span class="sxs-lookup"><span data-stu-id="85501-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="85501-198">-WebhookReceiver</span></span>
<span data-ttu-id="85501-199">Anger att du vill skapa en webhook-mottagare</span><span class="sxs-lookup"><span data-stu-id="85501-199">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="85501-200">-WebhookResourceId</span></span>
<span data-ttu-id="85501-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="85501-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="85501-202">-WorkspaceId</span></span>
<span data-ttu-id="85501-203">ID för ITSM arbets yta</span><span class="sxs-lookup"><span data-stu-id="85501-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85501-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85501-204">CommonParameters</span></span>
<span data-ttu-id="85501-205">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85501-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85501-206">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85501-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85501-207">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85501-207">INPUTS</span></span>

### <span data-ttu-id="85501-208">System. String</span><span class="sxs-lookup"><span data-stu-id="85501-208">System.String</span></span>

### <span data-ttu-id="85501-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85501-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="85501-210">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85501-210">OUTPUTS</span></span>

### <span data-ttu-id="85501-211">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="85501-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="85501-212">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85501-212">NOTES</span></span>

## <span data-ttu-id="85501-213">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85501-213">RELATED LINKS</span></span>

<span data-ttu-id="85501-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="85501-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
