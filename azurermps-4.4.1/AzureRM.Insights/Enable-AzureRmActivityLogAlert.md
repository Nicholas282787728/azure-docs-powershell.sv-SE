---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92607537fb80132627e1f26f240a10b8f7150fb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585524"
---
# <span data-ttu-id="9184b-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9184b-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="9184b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9184b-102">SYNOPSIS</span></span>
<span data-ttu-id="9184b-103">Aktiverar en aktivitets logg varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="9184b-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9184b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9184b-104">SYNTAX</span></span>

### <span data-ttu-id="9184b-105">Standard parametrar för att aktivera en aktivitets loggs avisering</span><span class="sxs-lookup"><span data-stu-id="9184b-105">Default parameters for enable an activity log alert</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9184b-106">Parametrar för att aktivera en aktivitets logg meddelanden som tar ett värde från en pipe</span><span class="sxs-lookup"><span data-stu-id="9184b-106">Parameters to enable an activity log alerts taking value from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9184b-107">Parametrar för att aktivera en aktivitets logg meddelanden som tar värdet av ResourceId från pipe</span><span class="sxs-lookup"><span data-stu-id="9184b-107">Parameters to enable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9184b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9184b-108">DESCRIPTION</span></span>
<span data-ttu-id="9184b-109">Med cmdleten **Enable-AzureRmActivityLogAlert** kan du aktivera en aktivitets loggs avisering och ange dess taggar.</span><span class="sxs-lookup"><span data-stu-id="9184b-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="9184b-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="9184b-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="9184b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9184b-111">EXAMPLES</span></span>

### <span data-ttu-id="9184b-112">Exempel 1: inaktivera en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="9184b-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="9184b-113">Det här kommandot aktiverar aviseringen för aktivitets loggen med namnet alert1 i resurs gruppen standard-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="9184b-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="9184b-114">Exempel 2: Aktivera en aktivitets logg varning med ett PSActivityLogAlertResource-objekt som inmatning</span><span class="sxs-lookup"><span data-stu-id="9184b-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="9184b-115">Det här kommandot aktiverar en aktivitets loggs avisering med namnet alert1.</span><span class="sxs-lookup"><span data-stu-id="9184b-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="9184b-116">För den här funktionen används ett PSActivityLogAlertResource-objekt som indataargument.</span><span class="sxs-lookup"><span data-stu-id="9184b-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="9184b-117">Exempel 3: Aktivera ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="9184b-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="9184b-118">Det här kommandot aktiverar ActivityLogAlert med hjälp av parametern ResourceId från pipe.</span><span class="sxs-lookup"><span data-stu-id="9184b-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="9184b-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9184b-119">PARAMETERS</span></span>

### <span data-ttu-id="9184b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9184b-120">-Name</span></span>
<span data-ttu-id="9184b-121">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="9184b-121">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9184b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9184b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9184b-123">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="9184b-123">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9184b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9184b-124">-InputObject</span></span>
<span data-ttu-id="9184b-125">Anger egenskapen InputObject Tags för samtalet för att extrahera obligatoriskt namn, resurs grupp namn och valfria egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9184b-125">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to enable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9184b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9184b-126">-ResourceId</span></span>
<span data-ttu-id="9184b-127">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9184b-127">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to enable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9184b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9184b-128">-Confirm</span></span>
<span data-ttu-id="9184b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9184b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9184b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9184b-130">-DefaultProfile</span></span>
<span data-ttu-id="9184b-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9184b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9184b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9184b-132">-WhatIf</span></span>
<span data-ttu-id="9184b-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9184b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9184b-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9184b-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9184b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9184b-135">CommonParameters</span></span>
<span data-ttu-id="9184b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9184b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9184b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9184b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9184b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9184b-138">INPUTS</span></span>

## <span data-ttu-id="9184b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9184b-139">OUTPUTS</span></span>

### <span data-ttu-id="9184b-140">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="9184b-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="9184b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9184b-141">NOTES</span></span>

## <span data-ttu-id="9184b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9184b-142">RELATED LINKS</span></span>

[<span data-ttu-id="9184b-143">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9184b-143">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9184b-144">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9184b-144">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9184b-145">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9184b-145">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9184b-146">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9184b-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="9184b-147">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9184b-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="9184b-148">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9184b-148">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
