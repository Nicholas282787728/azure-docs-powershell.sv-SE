---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: aff12a6bf8c5cfeb79186eef7df0880b9225d433
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261386"
---
# <span data-ttu-id="e2b5a-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2b5a-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e2b5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b5a-103">Tar bort ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e2b5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2b5a-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2b5a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b5a-106">Cmdleten **Remove-AzDataLakeAnalyticsAccount** tar bort ett Azure Data Lake Analytics-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e2b5a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b5a-108">Exempel 1: ta bort ett konto</span><span class="sxs-lookup"><span data-stu-id="e2b5a-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="e2b5a-109">Detta kommando tar bort det angivna data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="e2b5a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="e2b5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b5a-111">-DefaultProfile</span></span>
<span data-ttu-id="e2b5a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e2b5a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2b5a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e2b5a-113">-Force</span></span>
<span data-ttu-id="e2b5a-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b5a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2b5a-115">-Name</span></span>
<span data-ttu-id="e2b5a-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b5a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2b5a-117">-PassThru</span></span>
<span data-ttu-id="e2b5a-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e2b5a-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b5a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b5a-120">-ResourceGroupName</span></span>
<span data-ttu-id="e2b5a-121">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b5a-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2b5a-122">-Confirm</span></span>
<span data-ttu-id="e2b5a-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b5a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b5a-124">-WhatIf</span></span>
<span data-ttu-id="e2b5a-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b5a-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b5a-127">CommonParameters</span></span>
<span data-ttu-id="e2b5a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b5a-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2b5a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b5a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2b5a-130">INPUTS</span></span>

### <span data-ttu-id="e2b5a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e2b5a-131">System.String</span></span>

## <span data-ttu-id="e2b5a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2b5a-132">OUTPUTS</span></span>

### <span data-ttu-id="e2b5a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2b5a-133">System.Boolean</span></span>

## <span data-ttu-id="e2b5a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2b5a-134">NOTES</span></span>

## <span data-ttu-id="e2b5a-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2b5a-135">RELATED LINKS</span></span>

[<span data-ttu-id="e2b5a-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2b5a-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e2b5a-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2b5a-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e2b5a-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2b5a-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e2b5a-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e2b5a-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


