---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: dd84c2b12af850cc38770243df74a6bd25c205f3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929429"
---
# <span data-ttu-id="d43a6-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d43a6-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="d43a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d43a6-102">SYNOPSIS</span></span>
<span data-ttu-id="d43a6-103">Inaktiverar en aktivitets loggs varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="d43a6-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d43a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d43a6-104">SYNTAX</span></span>

### <span data-ttu-id="d43a6-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d43a6-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d43a6-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="d43a6-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d43a6-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="d43a6-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d43a6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d43a6-108">DESCRIPTION</span></span>
<span data-ttu-id="d43a6-109">Cmdleten **disable-AzureRmActivityLogAlert** inaktive ras och aktivitetens loggning gör det möjligt att ange dess taggar.</span><span class="sxs-lookup"><span data-stu-id="d43a6-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="d43a6-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="d43a6-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="d43a6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d43a6-111">EXAMPLES</span></span>

### <span data-ttu-id="d43a6-112">Exempel 1: inaktivera en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="d43a6-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="d43a6-113">Det här kommandot inaktiverar aktivitets logg varningen med namnet alert1 i resurs gruppen standard-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="d43a6-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="d43a6-114">Det här kommandot ändrar egenskapen taggar för aviseringen för aktivitets loggen med namnet alert1 och inaktiverar den.</span><span class="sxs-lookup"><span data-stu-id="d43a6-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="d43a6-115">Exempel 2: inaktivera en aktivitets logg varning med ett PSActivityLogAlertResource-objekt som inmatning</span><span class="sxs-lookup"><span data-stu-id="d43a6-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="d43a6-116">Det här kommandot inaktiverar en aktivitets loggs avisering med namnet alert1.</span><span class="sxs-lookup"><span data-stu-id="d43a6-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="d43a6-117">För den här funktionen används ett PSActivityLogAlertResource-objekt som indataargument.</span><span class="sxs-lookup"><span data-stu-id="d43a6-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="d43a6-118">Exempel 3: inaktivera ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="d43a6-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="d43a6-119">Det här kommandot inaktiverar ActivityLogAlert med hjälp av parametern ResourceId från pipe.</span><span class="sxs-lookup"><span data-stu-id="d43a6-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="d43a6-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d43a6-120">PARAMETERS</span></span>

### <span data-ttu-id="d43a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43a6-121">-DefaultProfile</span></span>
<span data-ttu-id="d43a6-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d43a6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d43a6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d43a6-123">-InputObject</span></span>
<span data-ttu-id="d43a6-124">Anger egenskapen InputObject Tags för samtalet för att extrahera obligatoriskt namn, resurs grupp namn och valfria Taggegenskaper.</span><span class="sxs-lookup"><span data-stu-id="d43a6-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d43a6-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d43a6-125">-Name</span></span>
<span data-ttu-id="d43a6-126">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="d43a6-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d43a6-128">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="d43a6-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43a6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d43a6-129">-ResourceId</span></span>
<span data-ttu-id="d43a6-130">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d43a6-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d43a6-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d43a6-131">-Confirm</span></span>
<span data-ttu-id="d43a6-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d43a6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d43a6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43a6-133">-WhatIf</span></span>
<span data-ttu-id="d43a6-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d43a6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d43a6-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d43a6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d43a6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43a6-136">CommonParameters</span></span>
<span data-ttu-id="d43a6-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43a6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43a6-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43a6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43a6-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d43a6-139">INPUTS</span></span>

### <span data-ttu-id="d43a6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d43a6-140">System.String</span></span>

### <span data-ttu-id="d43a6-141">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="d43a6-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="d43a6-142">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d43a6-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d43a6-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d43a6-143">OUTPUTS</span></span>

### <span data-ttu-id="d43a6-144">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="d43a6-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="d43a6-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d43a6-145">NOTES</span></span>

## <span data-ttu-id="d43a6-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d43a6-146">RELATED LINKS</span></span>

[<span data-ttu-id="d43a6-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d43a6-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d43a6-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d43a6-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d43a6-149">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d43a6-149">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d43a6-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="d43a6-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="d43a6-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="d43a6-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="d43a6-152">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d43a6-152">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
