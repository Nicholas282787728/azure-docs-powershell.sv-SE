---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 04112d84acb8b18ef4251aae86b9bdd00924993a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573430"
---
# <span data-ttu-id="ed55d-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed55d-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="ed55d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed55d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed55d-103">Hämtar notifieringsregler.</span><span class="sxs-lookup"><span data-stu-id="ed55d-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed55d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed55d-104">SYNTAX</span></span>

### <span data-ttu-id="ed55d-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ed55d-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed55d-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="ed55d-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed55d-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="ed55d-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed55d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed55d-108">DESCRIPTION</span></span>
<span data-ttu-id="ed55d-109">Cmdleten **Get-AzureRmAlertRule** hämtar en notifieringsregel efter dess namn eller URI, eller alla notifieringsregler från en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ed55d-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="ed55d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed55d-110">EXAMPLES</span></span>

### <span data-ttu-id="ed55d-111">Exempel 1: Hämta notifieringsregler för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ed55d-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="ed55d-112">Med det här kommandot får du alla notifieringsregler för resurs gruppen standard-Web-centrala.</span><span class="sxs-lookup"><span data-stu-id="ed55d-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="ed55d-113">Utdata innehåller inte information om reglerna eftersom parametern *DetailedOutput* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="ed55d-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="ed55d-114">Exempel 2: Hämta en notifieringsregel efter namn</span><span class="sxs-lookup"><span data-stu-id="ed55d-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="ed55d-115">Det här kommandot får notifieringsregeln med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="ed55d-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ed55d-116">Eftersom parametern *DetailedOutput* inte anges innehåller utdata bara grundläggande information om notifieringsregeln.</span><span class="sxs-lookup"><span data-stu-id="ed55d-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="ed55d-117">Exempel 3: Hämta en notifieringsregel efter namn med detaljerad utskrift</span><span class="sxs-lookup"><span data-stu-id="ed55d-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="ed55d-118">Det här kommandot får notifieringsregeln med namnet avisering-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="ed55d-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ed55d-119">Parametern *DetailedOutput* anges så att utdata är detaljerad.</span><span class="sxs-lookup"><span data-stu-id="ed55d-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="ed55d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed55d-120">PARAMETERS</span></span>

### <span data-ttu-id="ed55d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed55d-121">-DefaultProfile</span></span>
<span data-ttu-id="ed55d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ed55d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed55d-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="ed55d-123">-DetailedOutput</span></span>
<span data-ttu-id="ed55d-124">Visar alla detaljer i resultatet.</span><span class="sxs-lookup"><span data-stu-id="ed55d-124">Displays full details in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed55d-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed55d-125">-Name</span></span>
<span data-ttu-id="ed55d-126">Anger namnet på den notifieringsregel som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ed55d-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed55d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed55d-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed55d-128">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ed55d-128">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed55d-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ed55d-129">-TargetResourceId</span></span>
<span data-ttu-id="ed55d-130">Anger ID för mål resursen.</span><span class="sxs-lookup"><span data-stu-id="ed55d-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceUri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed55d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed55d-131">CommonParameters</span></span>
<span data-ttu-id="ed55d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed55d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed55d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed55d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed55d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed55d-134">INPUTS</span></span>

### <span data-ttu-id="ed55d-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="ed55d-135">None</span></span>
<span data-ttu-id="ed55d-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ed55d-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed55d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed55d-137">OUTPUTS</span></span>

### <span data-ttu-id="ed55d-138">List<Microsoft. Azure.-kommandon. Insights. OutputClasses. PSAlertRule></span><span class="sxs-lookup"><span data-stu-id="ed55d-138">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule></span></span>

## <span data-ttu-id="ed55d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed55d-139">NOTES</span></span>

## <span data-ttu-id="ed55d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed55d-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed55d-141">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed55d-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="ed55d-142">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed55d-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="ed55d-143">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed55d-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="ed55d-144">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ed55d-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="ed55d-145">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed55d-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


