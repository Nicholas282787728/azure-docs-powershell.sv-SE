---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271834"
---
# <span data-ttu-id="ae7b2-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae7b2-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="ae7b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7b2-103">Hämtar notifieringsregler.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-103">Gets alert rules.</span></span>

## <span data-ttu-id="ae7b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae7b2-104">SYNTAX</span></span>

### <span data-ttu-id="ae7b2-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae7b2-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae7b2-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="ae7b2-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae7b2-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="ae7b2-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae7b2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae7b2-108">DESCRIPTION</span></span>
<span data-ttu-id="ae7b2-109">Cmdleten **Get-AzAlertRule** hämtar en notifieringsregel efter dess namn eller URI, eller alla notifieringsregler från en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="ae7b2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae7b2-110">EXAMPLES</span></span>

### <span data-ttu-id="ae7b2-111">Exempel 1: Hämta notifieringsregler för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ae7b2-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="ae7b2-112">Med det här kommandot får du alla notifieringsregler för resurs gruppen standard-Web-centrala.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="ae7b2-113">Utdata innehåller inte information om reglerna eftersom parametern *DetailedOutput* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="ae7b2-114">Exempel 2: Hämta en notifieringsregel efter namn</span><span class="sxs-lookup"><span data-stu-id="ae7b2-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="ae7b2-115">Det här kommandot får notifieringsregeln med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ae7b2-116">Eftersom parametern *DetailedOutput* inte anges innehåller utdata bara grundläggande information om notifieringsregeln.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="ae7b2-117">Exempel 3: Hämta en notifieringsregel efter namn med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="ae7b2-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="ae7b2-118">Det här kommandot får notifieringsregeln med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ae7b2-119">Parametern *DetailedOutput* anges så att utdata är detaljerad.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="ae7b2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae7b2-120">PARAMETERS</span></span>

### <span data-ttu-id="ae7b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7b2-121">-DefaultProfile</span></span>
<span data-ttu-id="ae7b2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ae7b2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae7b2-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="ae7b2-123">-DetailedOutput</span></span>
<span data-ttu-id="ae7b2-124">Visar alla detaljer i resultatet.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="ae7b2-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae7b2-125">-Name</span></span>
<span data-ttu-id="ae7b2-126">Anger namnet på den notifieringsregel som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae7b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="ae7b2-128">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7b2-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ae7b2-129">-TargetResourceId</span></span>
<span data-ttu-id="ae7b2-130">Anger ID för mål resursen.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7b2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7b2-131">CommonParameters</span></span>
<span data-ttu-id="ae7b2-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7b2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7b2-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae7b2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7b2-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae7b2-134">INPUTS</span></span>

### <span data-ttu-id="ae7b2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ae7b2-135">System.String</span></span>

### <span data-ttu-id="ae7b2-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae7b2-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae7b2-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae7b2-137">OUTPUTS</span></span>

### <span data-ttu-id="ae7b2-138">Microsoft. Azure. commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae7b2-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="ae7b2-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae7b2-139">NOTES</span></span>

## <span data-ttu-id="ae7b2-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae7b2-140">RELATED LINKS</span></span>

[<span data-ttu-id="ae7b2-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae7b2-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="ae7b2-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae7b2-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="ae7b2-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae7b2-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="ae7b2-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ae7b2-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="ae7b2-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="ae7b2-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)

