---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5604430c795f7a318e18b89928c3a75d063a316a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576564"
---
# <span data-ttu-id="1c506-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1c506-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1c506-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c506-102">SYNOPSIS</span></span>
<span data-ttu-id="1c506-103">Tar bort en angiven beräknings princip för Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="1c506-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c506-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c506-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c506-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c506-105">DESCRIPTION</span></span>
<span data-ttu-id="1c506-106">**Remove-AzureRmDataLakeAnalyticsComputePolicy** tar bort en viss beräknings princip för Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="1c506-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="1c506-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c506-107">EXAMPLES</span></span>

### <span data-ttu-id="1c506-108">Exempel 1: ta bort en beräknings princip</span><span class="sxs-lookup"><span data-stu-id="1c506-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="1c506-109">Det här kommandot tar bort den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="1c506-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="1c506-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c506-110">PARAMETERS</span></span>

### <span data-ttu-id="1c506-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1c506-111">-Account</span></span>
<span data-ttu-id="1c506-112">Namnet på kontot som principen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="1c506-112">Name of the account to remove the compute policy from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c506-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c506-113">-DefaultProfile</span></span>
<span data-ttu-id="1c506-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1c506-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c506-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c506-115">-Name</span></span>
<span data-ttu-id="1c506-116">Namnet på den beräknings princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1c506-116">Name of the compute policy to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c506-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c506-117">-PassThru</span></span>
<span data-ttu-id="1c506-118">Returnerar true när du har tagit bort den.</span><span class="sxs-lookup"><span data-stu-id="1c506-118">Return true upon successful deletion.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c506-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c506-119">-ResourceGroupName</span></span>
<span data-ttu-id="1c506-120">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="1c506-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="1c506-121">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="1c506-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c506-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c506-122">-Confirm</span></span>
<span data-ttu-id="1c506-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c506-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c506-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c506-124">-WhatIf</span></span>
<span data-ttu-id="1c506-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c506-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c506-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1c506-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c506-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c506-127">CommonParameters</span></span>
<span data-ttu-id="1c506-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c506-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c506-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c506-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c506-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c506-130">INPUTS</span></span>

### <span data-ttu-id="1c506-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c506-131">System.String</span></span>

## <span data-ttu-id="1c506-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c506-132">OUTPUTS</span></span>

### <span data-ttu-id="1c506-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c506-133">System.Boolean</span></span>

## <span data-ttu-id="1c506-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c506-134">NOTES</span></span>

## <span data-ttu-id="1c506-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c506-135">RELATED LINKS</span></span>

