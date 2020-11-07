---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: cf920fe8fbe235a2c003bebc0cdecf1a480926ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758059"
---
# <span data-ttu-id="230c7-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="230c7-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="230c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="230c7-102">SYNOPSIS</span></span>
<span data-ttu-id="230c7-103">Inaktiverar en aktivitets loggs varning och anger dess taggar.</span><span class="sxs-lookup"><span data-stu-id="230c7-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="230c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="230c7-104">SYNTAX</span></span>

### <span data-ttu-id="230c7-105">Standard parametrar för inaktive ring av en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="230c7-105">Default parameters for disable an activity log alert</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="230c7-106">Parametrar för att inaktivera en aktivitets logg meddelanden som tar ett värde från en pipe</span><span class="sxs-lookup"><span data-stu-id="230c7-106">Parameters to disable an activity log alerts taking value from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="230c7-107">Parametrar för att inaktivera en aktivitets logg meddelanden som tar värdet av ResourceId från pipe</span><span class="sxs-lookup"><span data-stu-id="230c7-107">Parameters to disable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="230c7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="230c7-108">DESCRIPTION</span></span>
<span data-ttu-id="230c7-109">Cmdleten **disable-AzureRmActivityLogAlert** inaktive ras och aktivitetens loggning gör det möjligt att ange dess taggar.</span><span class="sxs-lookup"><span data-stu-id="230c7-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="230c7-110">Denna cmdlet implementerar ShouldProcess-mönstret, dvs. den kan begära bekräftelse från användaren innan han eller hon korrigerar resursen.</span><span class="sxs-lookup"><span data-stu-id="230c7-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="230c7-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="230c7-111">EXAMPLES</span></span>

### <span data-ttu-id="230c7-112">Exempel 1: inaktivera en aktivitets logg varning</span><span class="sxs-lookup"><span data-stu-id="230c7-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="230c7-113">Det här kommandot inaktiverar aktivitets logg varningen med namnet alert1 i resurs gruppen standard-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="230c7-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

<span data-ttu-id="230c7-114">Det här kommandot ändrar egenskapen taggar för aviseringen för aktivitets loggen med namnet alert1 och inaktiverar den.</span><span class="sxs-lookup"><span data-stu-id="230c7-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="230c7-115">Exempel 2: inaktivera en aktivitets logg varning med ett PSActivityLogAlertResource-objekt som inmatning</span><span class="sxs-lookup"><span data-stu-id="230c7-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="230c7-116">Det här kommandot inaktiverar en aktivitets loggs avisering med namnet alert1.</span><span class="sxs-lookup"><span data-stu-id="230c7-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="230c7-117">För den här funktionen används ett PSActivityLogAlertResource-objekt som indataargument.</span><span class="sxs-lookup"><span data-stu-id="230c7-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="230c7-118">Exempel 3: inaktivera ActivityLogAlert med parametern ResourceId</span><span class="sxs-lookup"><span data-stu-id="230c7-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="230c7-119">Det här kommandot inaktiverar ActivityLogAlert med hjälp av parametern ResourceId från pipe.</span><span class="sxs-lookup"><span data-stu-id="230c7-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="230c7-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="230c7-120">PARAMETERS</span></span>

### <span data-ttu-id="230c7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="230c7-121">-Name</span></span>
<span data-ttu-id="230c7-122">Namnet på aktivitets logg varningen.</span><span class="sxs-lookup"><span data-stu-id="230c7-122">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="230c7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230c7-123">-ResourceGroupName</span></span>
<span data-ttu-id="230c7-124">Namnet på resurs gruppen där aviserings resursen ska finnas.</span><span class="sxs-lookup"><span data-stu-id="230c7-124">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="230c7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="230c7-125">-InputObject</span></span>
<span data-ttu-id="230c7-126">Anger egenskapen InputObject Tags för samtalet för att extrahera obligatoriskt namn, resurs grupp namn och valfria Taggegenskaper.</span><span class="sxs-lookup"><span data-stu-id="230c7-126">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to disable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="230c7-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="230c7-127">-ResourceId</span></span>
<span data-ttu-id="230c7-128">Anger egenskapen ResourceId-taggar för samtalet för att extrahera namnet, resurs gruppens namn-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="230c7-128">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to disable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="230c7-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="230c7-129">-Confirm</span></span>
<span data-ttu-id="230c7-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="230c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="230c7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230c7-131">-DefaultProfile</span></span>
<span data-ttu-id="230c7-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="230c7-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="230c7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="230c7-133">-WhatIf</span></span>
<span data-ttu-id="230c7-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="230c7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="230c7-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="230c7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="230c7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230c7-136">CommonParameters</span></span>
<span data-ttu-id="230c7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="230c7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230c7-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="230c7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230c7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="230c7-139">INPUTS</span></span>

## <span data-ttu-id="230c7-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="230c7-140">OUTPUTS</span></span>

### <span data-ttu-id="230c7-141">Microsoft. Azure. commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="230c7-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="230c7-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="230c7-142">NOTES</span></span>

## <span data-ttu-id="230c7-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="230c7-143">RELATED LINKS</span></span>

[<span data-ttu-id="230c7-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="230c7-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="230c7-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="230c7-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="230c7-146">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="230c7-146">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="230c7-147">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="230c7-147">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="230c7-148">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="230c7-148">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="230c7-149">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="230c7-149">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
