---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931410"
---
# <span data-ttu-id="7e0d4-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e0d4-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="7e0d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0d4-103">Hämtar notifieringsregler.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e0d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e0d4-104">SYNTAX</span></span>

### <span data-ttu-id="7e0d4-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7e0d4-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e0d4-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="7e0d4-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e0d4-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="7e0d4-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e0d4-108">DESCRIPTION</span></span>
<span data-ttu-id="7e0d4-109">Cmdleten **Get-AzureRmAlertRule** hämtar en notifieringsregel efter dess namn eller URI, eller alla notifieringsregler från en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="7e0d4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e0d4-110">EXAMPLES</span></span>

### <span data-ttu-id="7e0d4-111">Exempel 1: Hämta notifieringsregler för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="7e0d4-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="7e0d4-112">Med det här kommandot får du alla notifieringsregler för resurs gruppen standard-Web-centrala.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="7e0d4-113">Utdata innehåller inte information om reglerna eftersom parametern *DetailedOutput* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="7e0d4-114">Exempel 2: Hämta en notifieringsregel efter namn</span><span class="sxs-lookup"><span data-stu-id="7e0d4-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="7e0d4-115">Det här kommandot får notifieringsregeln med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="7e0d4-116">Eftersom parametern *DetailedOutput* inte anges innehåller utdata bara grundläggande information om notifieringsregeln.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="7e0d4-117">Exempel 3: Hämta en notifieringsregel efter namn med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="7e0d4-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="7e0d4-118">Det här kommandot får notifieringsregeln med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="7e0d4-119">Parametern *DetailedOutput* anges så att utdata är detaljerad.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="7e0d4-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e0d4-120">PARAMETERS</span></span>

### <span data-ttu-id="7e0d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0d4-121">-DefaultProfile</span></span>
<span data-ttu-id="7e0d4-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7e0d4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e0d4-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="7e0d4-123">-DetailedOutput</span></span>
<span data-ttu-id="7e0d4-124">Visar alla detaljer i resultatet.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="7e0d4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e0d4-125">-Name</span></span>
<span data-ttu-id="7e0d4-126">Anger namnet på den notifieringsregel som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="7e0d4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0d4-127">-ResourceGroupName</span></span>
<span data-ttu-id="7e0d4-128">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7e0d4-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7e0d4-129">-TargetResourceId</span></span>
<span data-ttu-id="7e0d4-130">Anger ID för mål resursen.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="7e0d4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0d4-131">CommonParameters</span></span>
<span data-ttu-id="7e0d4-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0d4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0d4-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e0d4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0d4-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e0d4-134">INPUTS</span></span>

### <span data-ttu-id="7e0d4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7e0d4-135">System.String</span></span>

### <span data-ttu-id="7e0d4-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e0d4-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7e0d4-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e0d4-137">OUTPUTS</span></span>

### <span data-ttu-id="7e0d4-138">Microsoft. Azure. commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e0d4-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="7e0d4-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e0d4-139">NOTES</span></span>

## <span data-ttu-id="7e0d4-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e0d4-140">RELATED LINKS</span></span>



[<span data-ttu-id="7e0d4-141">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e0d4-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7e0d4-142">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e0d4-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7e0d4-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7e0d4-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="7e0d4-144">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7e0d4-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


