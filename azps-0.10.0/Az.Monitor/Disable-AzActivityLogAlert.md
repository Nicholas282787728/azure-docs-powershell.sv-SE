---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 84a377e2936a2c9f5aeaf0516dc96f848b9eb0b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922658"
---
# <span data-ttu-id="eeda7-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eeda7-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="eeda7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eeda7-102">SYNOPSIS</span></span>
<span data-ttu-id="eeda7-103">Inaktiverar en aktivitets loggs varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="eeda7-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="eeda7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eeda7-104">SYNTAX</span></span>

### <span data-ttu-id="eeda7-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eeda7-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeda7-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="eeda7-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeda7-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="eeda7-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eeda7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eeda7-108">DESCRIPTION</span></span>
<span data-ttu-id="eeda7-109">Cmdleten **disable-AzActivityLogAlert** inaktive ras och aktivitetens loggning gör det möjligt att ange dess taggar.</span><span class="sxs-lookup"><span data-stu-id="eeda7-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="eeda7-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="eeda7-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="eeda7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eeda7-111">EXAMPLES</span></span>

### <span data-ttu-id="eeda7-112">Exempel 1: inaktivera en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="eeda7-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="eeda7-113">Det här kommandot inaktiverar aktivitets logg varningen med namnet alert1 i resurs gruppen standard-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="eeda7-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="eeda7-114">Det här kommandot ändrar egenskapen taggar för aviseringen för aktivitets loggen med namnet alert1 och inaktiverar den.</span><span class="sxs-lookup"><span data-stu-id="eeda7-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="eeda7-115">Exempel 2: inaktivera en aktivitets logg varning med ett PSActivityLogAlertResource-objekt som inmatning</span><span class="sxs-lookup"><span data-stu-id="eeda7-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="eeda7-116">Det här kommandot inaktiverar en aktivitets loggs avisering med namnet alert1.</span><span class="sxs-lookup"><span data-stu-id="eeda7-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="eeda7-117">För den här funktionen används ett PSActivityLogAlertResource-objekt som indataargument.</span><span class="sxs-lookup"><span data-stu-id="eeda7-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="eeda7-118">Exempel 3: inaktivera ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeda7-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="eeda7-119">Det här kommandot inaktiverar ActivityLogAlert med hjälp av parametern ResourceId från pipe.</span><span class="sxs-lookup"><span data-stu-id="eeda7-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="eeda7-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eeda7-120">PARAMETERS</span></span>

### <span data-ttu-id="eeda7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeda7-121">-DefaultProfile</span></span>
<span data-ttu-id="eeda7-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="eeda7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeda7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eeda7-123">-InputObject</span></span>
<span data-ttu-id="eeda7-124">Anger egenskapen InputObject Tags för samtalet för att extrahera obligatoriskt namn, resurs grupp namn och valfria Taggegenskaper.</span><span class="sxs-lookup"><span data-stu-id="eeda7-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="eeda7-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="eeda7-125">-Name</span></span>
<span data-ttu-id="eeda7-126">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="eeda7-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="eeda7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeda7-127">-ResourceGroupName</span></span>
<span data-ttu-id="eeda7-128">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="eeda7-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="eeda7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeda7-129">-ResourceId</span></span>
<span data-ttu-id="eeda7-130">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="eeda7-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="eeda7-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eeda7-131">-Confirm</span></span>
<span data-ttu-id="eeda7-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eeda7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeda7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeda7-133">-WhatIf</span></span>
<span data-ttu-id="eeda7-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eeda7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeda7-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eeda7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeda7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeda7-136">CommonParameters</span></span>
<span data-ttu-id="eeda7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeda7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeda7-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeda7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeda7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eeda7-139">INPUTS</span></span>

### <span data-ttu-id="eeda7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eeda7-140">System.String</span></span>

### <span data-ttu-id="eeda7-141">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="eeda7-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="eeda7-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eeda7-142">OUTPUTS</span></span>

### <span data-ttu-id="eeda7-143">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="eeda7-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="eeda7-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eeda7-144">NOTES</span></span>

## <span data-ttu-id="eeda7-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eeda7-145">RELATED LINKS</span></span>

[<span data-ttu-id="eeda7-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eeda7-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="eeda7-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eeda7-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="eeda7-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eeda7-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="eeda7-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="eeda7-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="eeda7-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="eeda7-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="eeda7-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eeda7-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
