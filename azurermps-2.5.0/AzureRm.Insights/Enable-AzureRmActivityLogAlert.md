---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 856e3abc5cf99c7ae7f871619476717af21aed9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931433"
---
# <span data-ttu-id="a12f5-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a12f5-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="a12f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a12f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a12f5-103">Aktiverar en aktivitets logg varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="a12f5-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a12f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a12f5-104">SYNTAX</span></span>

### <span data-ttu-id="a12f5-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a12f5-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12f5-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="a12f5-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12f5-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="a12f5-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a12f5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a12f5-108">DESCRIPTION</span></span>
<span data-ttu-id="a12f5-109">Med cmdleten **Enable-AzureRmActivityLogAlert** kan du aktivera en aktivitets loggs avisering och ange dess taggar.</span><span class="sxs-lookup"><span data-stu-id="a12f5-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="a12f5-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="a12f5-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a12f5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a12f5-111">EXAMPLES</span></span>

### <span data-ttu-id="a12f5-112">Exempel 1: inaktivera en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="a12f5-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="a12f5-113">Det här kommandot aktiverar aviseringen för aktivitets loggen med namnet alert1 i resurs gruppen standard-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="a12f5-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="a12f5-114">Exempel 2: Aktivera en aktivitets logg varning med ett PSActivityLogAlertResource-objekt som inmatning</span><span class="sxs-lookup"><span data-stu-id="a12f5-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="a12f5-115">Det här kommandot aktiverar en aktivitets loggs avisering med namnet alert1.</span><span class="sxs-lookup"><span data-stu-id="a12f5-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="a12f5-116">För den här funktionen används ett PSActivityLogAlertResource-objekt som indataargument.</span><span class="sxs-lookup"><span data-stu-id="a12f5-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="a12f5-117">Exempel 3: Aktivera ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="a12f5-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="a12f5-118">Det här kommandot aktiverar ActivityLogAlert med hjälp av parametern ResourceId från pipe.</span><span class="sxs-lookup"><span data-stu-id="a12f5-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a12f5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a12f5-119">PARAMETERS</span></span>

### <span data-ttu-id="a12f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12f5-120">-DefaultProfile</span></span>
<span data-ttu-id="a12f5-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a12f5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a12f5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a12f5-122">-InputObject</span></span>
<span data-ttu-id="a12f5-123">Anger egenskapen InputObject Tags för samtalet för att extrahera obligatoriskt namn, resurs grupp namn och valfria egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a12f5-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a12f5-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a12f5-124">-Name</span></span>
<span data-ttu-id="a12f5-125">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="a12f5-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12f5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12f5-126">-ResourceGroupName</span></span>
<span data-ttu-id="a12f5-127">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="a12f5-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12f5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a12f5-128">-ResourceId</span></span>
<span data-ttu-id="a12f5-129">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a12f5-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12f5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a12f5-130">-Confirm</span></span>
<span data-ttu-id="a12f5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a12f5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a12f5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a12f5-132">-WhatIf</span></span>
<span data-ttu-id="a12f5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a12f5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a12f5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a12f5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a12f5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12f5-135">CommonParameters</span></span>
<span data-ttu-id="a12f5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a12f5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12f5-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a12f5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12f5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a12f5-138">INPUTS</span></span>

### <span data-ttu-id="a12f5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a12f5-139">System.String</span></span>

### <span data-ttu-id="a12f5-140">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a12f5-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="a12f5-141">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a12f5-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a12f5-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a12f5-142">OUTPUTS</span></span>

### <span data-ttu-id="a12f5-143">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a12f5-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a12f5-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a12f5-144">NOTES</span></span>

## <span data-ttu-id="a12f5-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a12f5-145">RELATED LINKS</span></span>

[<span data-ttu-id="a12f5-146">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a12f5-146">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a12f5-147">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a12f5-147">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a12f5-148">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a12f5-148">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a12f5-149">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a12f5-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="a12f5-150">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a12f5-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="a12f5-151">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a12f5-151">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
