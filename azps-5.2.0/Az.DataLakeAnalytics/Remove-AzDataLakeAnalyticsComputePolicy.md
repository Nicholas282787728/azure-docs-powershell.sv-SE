---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418123"
---
# <span data-ttu-id="09581-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="09581-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="09581-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09581-102">SYNOPSIS</span></span>
<span data-ttu-id="09581-103">Tar bort en angiven beräknings princip för Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="09581-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="09581-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09581-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09581-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09581-105">DESCRIPTION</span></span>
<span data-ttu-id="09581-106">**Remove-AzDataLakeAnalyticsComputePolicy** tar bort en viss beräknings princip för Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="09581-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="09581-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09581-107">EXAMPLES</span></span>

### <span data-ttu-id="09581-108">Exempel 1: ta bort en beräknings princip</span><span class="sxs-lookup"><span data-stu-id="09581-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="09581-109">Det här kommandot tar bort den angivna beräknings principen med namnet "policy" i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="09581-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="09581-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09581-110">PARAMETERS</span></span>

### <span data-ttu-id="09581-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="09581-111">-Account</span></span>
<span data-ttu-id="09581-112">Namnet på kontot som principen ska tas bort från.</span><span class="sxs-lookup"><span data-stu-id="09581-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="09581-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09581-113">-DefaultProfile</span></span>
<span data-ttu-id="09581-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="09581-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09581-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="09581-115">-Name</span></span>
<span data-ttu-id="09581-116">Namnet på den beräknings princip som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="09581-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="09581-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09581-117">-PassThru</span></span>
<span data-ttu-id="09581-118">Returnerar true när du har tagit bort den.</span><span class="sxs-lookup"><span data-stu-id="09581-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="09581-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09581-119">-ResourceGroupName</span></span>
<span data-ttu-id="09581-120">Namnet på den resurs grupp som du har kontot för.</span><span class="sxs-lookup"><span data-stu-id="09581-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="09581-121">Valfritt och försöker upptäcka om det inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="09581-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="09581-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09581-122">-Confirm</span></span>
<span data-ttu-id="09581-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09581-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09581-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09581-124">-WhatIf</span></span>
<span data-ttu-id="09581-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09581-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09581-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09581-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09581-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09581-127">CommonParameters</span></span>
<span data-ttu-id="09581-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09581-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09581-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09581-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09581-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09581-130">INPUTS</span></span>

### <span data-ttu-id="09581-131">System. String</span><span class="sxs-lookup"><span data-stu-id="09581-131">System.String</span></span>

## <span data-ttu-id="09581-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09581-132">OUTPUTS</span></span>

### <span data-ttu-id="09581-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09581-133">System.Boolean</span></span>

## <span data-ttu-id="09581-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09581-134">NOTES</span></span>

## <span data-ttu-id="09581-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09581-135">RELATED LINKS</span></span>
