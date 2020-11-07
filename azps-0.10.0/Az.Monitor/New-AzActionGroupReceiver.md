---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: e795f54fbcd31a8035e892a545b4afa1c2283366
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922590"
---
# <span data-ttu-id="3272e-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="3272e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3272e-102">SYNOPSIS</span></span>
<span data-ttu-id="3272e-103">Skapar en ny mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="3272e-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="3272e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3272e-104">SYNTAX</span></span>

### <span data-ttu-id="3272e-105">NewEmailReceiver (standard)</span><span class="sxs-lookup"><span data-stu-id="3272e-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3272e-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3272e-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3272e-115">DESCRIPTION</span></span>
<span data-ttu-id="3272e-116">Cmdleten **New-AzActionGroupReceiver** skapar en ny grupp mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="3272e-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="3272e-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3272e-117">EXAMPLES</span></span>

### <span data-ttu-id="3272e-118">Exempel 1: skapa en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="3272e-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="3272e-119">Det här kommandot skapar en ny e-postmottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="3272e-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="3272e-120">Exempel 2: skapa en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="3272e-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="3272e-121">Det här kommandot skapar en ny SMS-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="3272e-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="3272e-122">Exempel 3: skapa en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="3272e-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="3272e-123">Det här kommandot skapar en ny webhook-mottagare i minnet.</span><span class="sxs-lookup"><span data-stu-id="3272e-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="3272e-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3272e-124">PARAMETERS</span></span>

### <span data-ttu-id="3272e-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="3272e-126">Skapa en ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="3272e-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="3272e-127">-AutomationAccountId</span></span>
<span data-ttu-id="3272e-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="3272e-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="3272e-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="3272e-130">Skapa en AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="3272e-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="3272e-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="3272e-132">URI: n där webhookarna ska skickas</span><span class="sxs-lookup"><span data-stu-id="3272e-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="3272e-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3272e-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="3272e-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3272e-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="3272e-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="3272e-136">Skapa en AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="3272e-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="3272e-138">Skapa en ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="3272e-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="3272e-139">-CallbackUrl</span></span>
<span data-ttu-id="3272e-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="3272e-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="3272e-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="3272e-141">-ConnectionId</span></span>
<span data-ttu-id="3272e-142">ITSM anslutnings-ID för denna mottagare</span><span class="sxs-lookup"><span data-stu-id="3272e-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="3272e-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="3272e-143">-CountryCode</span></span>
<span data-ttu-id="3272e-144">Anger lands koden för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="3272e-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="3272e-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3272e-145">-DefaultProfile</span></span>
<span data-ttu-id="3272e-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3272e-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3272e-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3272e-147">-EmailAddress</span></span>
<span data-ttu-id="3272e-148">Anger adressen för e-postmottagaren.</span><span class="sxs-lookup"><span data-stu-id="3272e-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="3272e-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-149">-EmailReceiver</span></span>
<span data-ttu-id="3272e-150">Anger att du vill skapa en e-postmottagare</span><span class="sxs-lookup"><span data-stu-id="3272e-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="3272e-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="3272e-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="3272e-152">programmet resourceId för funktioner</span><span class="sxs-lookup"><span data-stu-id="3272e-152">the function app resourceId</span></span>

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

### <span data-ttu-id="3272e-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="3272e-153">-FunctionName</span></span>
<span data-ttu-id="3272e-154">functionName</span><span class="sxs-lookup"><span data-stu-id="3272e-154">the functionName</span></span>

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

### <span data-ttu-id="3272e-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="3272e-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="3272e-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="3272e-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="3272e-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="3272e-157">-IdentifierUri</span></span>
<span data-ttu-id="3272e-158">ID för identitets-URI för AAD auth</span><span class="sxs-lookup"><span data-stu-id="3272e-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="3272e-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="3272e-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="3272e-160">visar om den här instansen är en global Runbook</span><span class="sxs-lookup"><span data-stu-id="3272e-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="3272e-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-161">-ItsmReceiver</span></span>
<span data-ttu-id="3272e-162">Skapa en ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="3272e-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-163">-LogicAppReceiver</span></span>
<span data-ttu-id="3272e-164">Skapa en LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="3272e-165">-Namn</span><span class="sxs-lookup"><span data-stu-id="3272e-165">-Name</span></span>
<span data-ttu-id="3272e-166">Anger namnet på mottagaren.</span><span class="sxs-lookup"><span data-stu-id="3272e-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="3272e-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3272e-167">-ObjectId</span></span>
<span data-ttu-id="3272e-168">webhook-programobjekt-ID för AAD auth</span><span class="sxs-lookup"><span data-stu-id="3272e-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="3272e-169">-Telefonnummer</span><span class="sxs-lookup"><span data-stu-id="3272e-169">-PhoneNumber</span></span>
<span data-ttu-id="3272e-170">Anger telefonnumret för SMS-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="3272e-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="3272e-171">-Region</span><span class="sxs-lookup"><span data-stu-id="3272e-171">-Region</span></span>
<span data-ttu-id="3272e-172">ITSM region för denna mottagare</span><span class="sxs-lookup"><span data-stu-id="3272e-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="3272e-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3272e-173">-ResourceId</span></span>
<span data-ttu-id="3272e-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3272e-174">the ResourceId</span></span>

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

### <span data-ttu-id="3272e-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="3272e-175">-RoleId</span></span>
<span data-ttu-id="3272e-176">Mottagarens roll-ID</span><span class="sxs-lookup"><span data-stu-id="3272e-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="3272e-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="3272e-177">-RunbookName</span></span>
<span data-ttu-id="3272e-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="3272e-178">the RunbookName</span></span>

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

### <span data-ttu-id="3272e-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="3272e-179">-ServiceUri</span></span>
<span data-ttu-id="3272e-180">Anger URI för webhook-mottagaren.</span><span class="sxs-lookup"><span data-stu-id="3272e-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="3272e-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-181">-SmsReceiver</span></span>
<span data-ttu-id="3272e-182">Anger att SMS-mottagare ska skapas</span><span class="sxs-lookup"><span data-stu-id="3272e-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="3272e-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="3272e-183">-TenantId</span></span>
<span data-ttu-id="3272e-184">klient-ID för AAD auth</span><span class="sxs-lookup"><span data-stu-id="3272e-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="3272e-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="3272e-185">-TicketConfiguration</span></span>
<span data-ttu-id="3272e-186">ITSM TicketConfiguration för denna mottagare</span><span class="sxs-lookup"><span data-stu-id="3272e-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="3272e-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="3272e-187">-UseAadAuth</span></span>
<span data-ttu-id="3272e-188">flaggan för att lägga till auth</span><span class="sxs-lookup"><span data-stu-id="3272e-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="3272e-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="3272e-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="3272e-190">Flaggan som används för att använda vanligt aviserings schema.</span><span class="sxs-lookup"><span data-stu-id="3272e-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="3272e-191">Det här värdet kommer att vara neglectedfor SMS, Azure App push, ITSM och Voice recievers.</span><span class="sxs-lookup"><span data-stu-id="3272e-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="3272e-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="3272e-192">-VoiceCountryCode</span></span>
<span data-ttu-id="3272e-193">Land koden för röst mottagaren</span><span class="sxs-lookup"><span data-stu-id="3272e-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="3272e-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="3272e-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="3272e-195">Telefonnumret till röst mottagaren</span><span class="sxs-lookup"><span data-stu-id="3272e-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="3272e-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-196">-VoiceReceiver</span></span>
<span data-ttu-id="3272e-197">Skapa en röst mottagare</span><span class="sxs-lookup"><span data-stu-id="3272e-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="3272e-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="3272e-198">-WebhookReceiver</span></span>
<span data-ttu-id="3272e-199">Anger att du vill skapa en webhook-mottagare</span><span class="sxs-lookup"><span data-stu-id="3272e-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="3272e-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="3272e-200">-WebhookResourceId</span></span>
<span data-ttu-id="3272e-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="3272e-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="3272e-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="3272e-202">-WorkspaceId</span></span>
<span data-ttu-id="3272e-203">ID för ITSM arbets yta</span><span class="sxs-lookup"><span data-stu-id="3272e-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="3272e-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3272e-204">CommonParameters</span></span>
<span data-ttu-id="3272e-205">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3272e-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3272e-206">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3272e-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3272e-207">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3272e-207">INPUTS</span></span>

### <span data-ttu-id="3272e-208">System. String</span><span class="sxs-lookup"><span data-stu-id="3272e-208">System.String</span></span>

### <span data-ttu-id="3272e-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3272e-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3272e-210">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3272e-210">OUTPUTS</span></span>

### <span data-ttu-id="3272e-211">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="3272e-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="3272e-212">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3272e-212">NOTES</span></span>

## <span data-ttu-id="3272e-213">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3272e-213">RELATED LINKS</span></span>

<span data-ttu-id="3272e-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="3272e-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
