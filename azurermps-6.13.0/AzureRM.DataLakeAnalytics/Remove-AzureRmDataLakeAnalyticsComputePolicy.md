---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: a97c6835144cda227fc07645f087e393cda2b8f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575233"
---
# <span data-ttu-id="6b823-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="6b823-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="6b823-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b823-102">SYNOPSIS</span></span>
<span data-ttu-id="6b823-103">Tar bort en angiven beräknings princip för Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="6b823-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b823-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b823-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b823-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b823-105">DESCRIPTION</span></span>
<span data-ttu-id="6b823-106">**Remove-AzureRmDataLakeAnalyticsComputePolicy** tar bort en viss beräknings princip för Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b823-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="6b823-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b823-107">EXAMPLES</span></span>

### <span data-ttu-id="6b823-108">Exempel 1: ta bort en beräknings princip</span><span class="sxs-lookup"><span data-stu-id="6b823-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="6b823-109">Det här kommandot tar bort den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="6b823-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="6b823-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b823-110">PARAMETERS</span></span>

### <span data-ttu-id="6b823-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="6b823-111">-Account</span></span>
<span data-ttu-id="6b823-112">Namnet på kontot som principen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="6b823-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b823-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b823-113">-DefaultProfile</span></span>
<span data-ttu-id="6b823-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6b823-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b823-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="6b823-115">-Name</span></span>
<span data-ttu-id="6b823-116">Namnet på den beräknings princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6b823-116">Name of the compute policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b823-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b823-117">-PassThru</span></span>
<span data-ttu-id="6b823-118">Returnerar true när du har tagit bort den.</span><span class="sxs-lookup"><span data-stu-id="6b823-118">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b823-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b823-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b823-120">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="6b823-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="6b823-121">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="6b823-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="6b823-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6b823-122">-Confirm</span></span>
<span data-ttu-id="6b823-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b823-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b823-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b823-124">-WhatIf</span></span>
<span data-ttu-id="6b823-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6b823-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b823-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6b823-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b823-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b823-127">CommonParameters</span></span>
<span data-ttu-id="6b823-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b823-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b823-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b823-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b823-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b823-130">INPUTS</span></span>

### <span data-ttu-id="6b823-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6b823-131">System.String</span></span>

## <span data-ttu-id="6b823-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b823-132">OUTPUTS</span></span>

### <span data-ttu-id="6b823-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b823-133">System.Boolean</span></span>

## <span data-ttu-id="6b823-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b823-134">NOTES</span></span>

## <span data-ttu-id="6b823-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b823-135">RELATED LINKS</span></span>
