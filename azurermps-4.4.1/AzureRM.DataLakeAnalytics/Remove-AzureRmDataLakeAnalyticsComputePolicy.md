---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 8be60712f0687edcbd036c48a079e3ecb90ec6c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582492"
---
# <span data-ttu-id="4fa06-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4fa06-101">Remove-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4fa06-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fa06-102">SYNOPSIS</span></span>
<span data-ttu-id="4fa06-103">Tar bort en angiven beräknings princip för Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4fa06-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fa06-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fa06-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fa06-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fa06-105">DESCRIPTION</span></span>
<span data-ttu-id="4fa06-106">**Remove-AzureRmDataLakeAnalyticsComputePolicy** tar bort en viss beräknings princip för Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4fa06-106">The **Remove-AzureRmDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="4fa06-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fa06-107">EXAMPLES</span></span>

### <span data-ttu-id="4fa06-108">Exempel 1: ta bort en beräknings princip</span><span class="sxs-lookup"><span data-stu-id="4fa06-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="4fa06-109">Det här kommandot tar bort den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="4fa06-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="4fa06-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fa06-110">PARAMETERS</span></span>

### <span data-ttu-id="4fa06-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="4fa06-111">-Account</span></span>
<span data-ttu-id="4fa06-112">Namnet på kontot som principen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="4fa06-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="4fa06-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="4fa06-113">-Name</span></span>
<span data-ttu-id="4fa06-114">Namnet på den beräknings princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4fa06-114">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="4fa06-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fa06-115">-PassThru</span></span>
<span data-ttu-id="4fa06-116">Returnerar true när du har tagit bort den.</span><span class="sxs-lookup"><span data-stu-id="4fa06-116">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="4fa06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fa06-117">-ResourceGroupName</span></span>
<span data-ttu-id="4fa06-118">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="4fa06-118">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="4fa06-119">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="4fa06-119">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="4fa06-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4fa06-120">-Confirm</span></span>
<span data-ttu-id="4fa06-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fa06-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fa06-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fa06-122">-WhatIf</span></span>
<span data-ttu-id="4fa06-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4fa06-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fa06-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4fa06-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fa06-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fa06-125">-DefaultProfile</span></span>
<span data-ttu-id="4fa06-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fa06-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fa06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fa06-127">CommonParameters</span></span>
<span data-ttu-id="4fa06-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fa06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fa06-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fa06-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fa06-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fa06-130">INPUTS</span></span>

### <span data-ttu-id="4fa06-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4fa06-131">System.String</span></span>

## <span data-ttu-id="4fa06-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fa06-132">OUTPUTS</span></span>

### <span data-ttu-id="4fa06-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fa06-133">System.Boolean</span></span>

## <span data-ttu-id="4fa06-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fa06-134">NOTES</span></span>

## <span data-ttu-id="4fa06-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fa06-135">RELATED LINKS</span></span>

