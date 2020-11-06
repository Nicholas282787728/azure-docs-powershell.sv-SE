---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585540"
---
# <span data-ttu-id="f9a47-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a47-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="f9a47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9a47-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a47-103">Lägger till eller ersätter en regel för loggnings aviseringar.</span><span class="sxs-lookup"><span data-stu-id="f9a47-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9a47-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9a47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9a47-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a47-106">Cmdleten **Add-AzureRmLogAlertRule** lägger till eller ersätter en varnings regel för händelser.</span><span class="sxs-lookup"><span data-stu-id="f9a47-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="f9a47-107">Den tillagda regeln associeras med en resurs grupp och har ett namn.</span><span class="sxs-lookup"><span data-stu-id="f9a47-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="f9a47-108">Som annonseras i tidigare versioner: **cmdleten Add-AzureRMLogAlertRule kommer att vara inaktuell i en senare version.**</span><span class="sxs-lookup"><span data-stu-id="f9a47-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="f9a47-109">Efter den 1 oktober 2017 har denna cmdlet inte längre någon effekt eftersom den här funktionen övergår till aktivitets loggs aviseringar.</span><span class="sxs-lookup"><span data-stu-id="f9a47-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="f9a47-110">**_https://aka.ms/migratemealerts_** Mer information finns i.</span><span class="sxs-lookup"><span data-stu-id="f9a47-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="f9a47-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9a47-111">EXAMPLES</span></span>

### <span data-ttu-id="f9a47-112">Exempel 1: lägga till en regel för loggnings varningar</span><span class="sxs-lookup"><span data-stu-id="f9a47-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="f9a47-113">Det här kommandot lägger till eller uppdaterar en Event-baserad notifieringsregel.</span><span class="sxs-lookup"><span data-stu-id="f9a47-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="f9a47-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9a47-114">PARAMETERS</span></span>

### <span data-ttu-id="f9a47-115">-Åtgärder</span><span class="sxs-lookup"><span data-stu-id="f9a47-115">-Actions</span></span>
<span data-ttu-id="f9a47-116">Anger en kommaavgränsad lista med åtgärder.</span><span class="sxs-lookup"><span data-stu-id="f9a47-116">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f9a47-117">-Description</span></span>
<span data-ttu-id="f9a47-118">Anger en beskrivning av regeln.</span><span class="sxs-lookup"><span data-stu-id="f9a47-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="f9a47-119">-DisableRule</span></span>
<span data-ttu-id="f9a47-120">Inaktiverar en regel.</span><span class="sxs-lookup"><span data-stu-id="f9a47-120">Disables a rule.</span></span>
<span data-ttu-id="f9a47-121">Om du inte anger den här parametern aktive ras regeln.</span><span class="sxs-lookup"><span data-stu-id="f9a47-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="f9a47-122">-Nivå</span><span class="sxs-lookup"><span data-stu-id="f9a47-122">-Level</span></span>
<span data-ttu-id="f9a47-123">Anger nivån för den händelse som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="f9a47-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="f9a47-124">Ange endast den här parametern för händelsebaserade regler.</span><span class="sxs-lookup"><span data-stu-id="f9a47-124">Specify this parameter only for event-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="f9a47-125">-Location</span></span>
<span data-ttu-id="f9a47-126">Anger platsen för regeln.</span><span class="sxs-lookup"><span data-stu-id="f9a47-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="f9a47-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f9a47-127">-Name</span></span>
<span data-ttu-id="f9a47-128">Anger namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="f9a47-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="f9a47-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="f9a47-129">-OperationName</span></span>
<span data-ttu-id="f9a47-130">Anger namnet på åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f9a47-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="f9a47-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9a47-131">-ResourceGroup</span></span>
<span data-ttu-id="f9a47-132">Anger namnet på resurs gruppen för regeln.</span><span class="sxs-lookup"><span data-stu-id="f9a47-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="f9a47-133">-Status</span><span class="sxs-lookup"><span data-stu-id="f9a47-133">-Status</span></span>
<span data-ttu-id="f9a47-134">Anger status.</span><span class="sxs-lookup"><span data-stu-id="f9a47-134">Specifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-135">Under status</span><span class="sxs-lookup"><span data-stu-id="f9a47-135">-SubStatus</span></span>
<span data-ttu-id="f9a47-136">Anger under statusen.</span><span class="sxs-lookup"><span data-stu-id="f9a47-136">Specifies the substatus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9a47-137">-TargetResourceGroup</span></span>
<span data-ttu-id="f9a47-138">Anger resurs gruppen för den resurs som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="f9a47-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f9a47-139">-TargetResourceId</span></span>
<span data-ttu-id="f9a47-140">Anger ID för den resurs som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="f9a47-140">Specifies the ID of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f9a47-141">-TargetResourceProvider</span></span>
<span data-ttu-id="f9a47-142">Anger resurs leverantören för den resurs som regeln övervakar.</span><span class="sxs-lookup"><span data-stu-id="f9a47-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a47-143">-DefaultProfile</span></span>
<span data-ttu-id="f9a47-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a47-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9a47-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a47-145">CommonParameters</span></span>
<span data-ttu-id="f9a47-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a47-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a47-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a47-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a47-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9a47-148">INPUTS</span></span>

## <span data-ttu-id="f9a47-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9a47-149">OUTPUTS</span></span>

### <span data-ttu-id="f9a47-150">Microsoft. Azure. commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f9a47-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="f9a47-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9a47-151">NOTES</span></span>

## <span data-ttu-id="f9a47-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9a47-152">RELATED LINKS</span></span>

[<span data-ttu-id="f9a47-153">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a47-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="f9a47-154">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a47-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="f9a47-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="f9a47-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="f9a47-156">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="f9a47-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="f9a47-157">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="f9a47-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


