---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a04295bca6c664e583ae9653b1f3ed7d52aebf3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757095"
---
# <span data-ttu-id="968b5-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="968b5-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="968b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="968b5-102">SYNOPSIS</span></span>
<span data-ttu-id="968b5-103">Tar bort ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="968b5-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="968b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="968b5-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="968b5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="968b5-105">DESCRIPTION</span></span>
<span data-ttu-id="968b5-106">Cmdleten **Remove-AzureRmDataLakeAnalyticsAccount** tar bort ett Azure Data Lake Analytics-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="968b5-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="968b5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="968b5-107">EXAMPLES</span></span>

### <span data-ttu-id="968b5-108">Exempel 1: ta bort ett konto</span><span class="sxs-lookup"><span data-stu-id="968b5-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="968b5-109">Detta kommando tar bort det angivna data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="968b5-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="968b5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="968b5-110">PARAMETERS</span></span>

### <span data-ttu-id="968b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968b5-111">-DefaultProfile</span></span>
<span data-ttu-id="968b5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="968b5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="968b5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="968b5-113">-Force</span></span>
<span data-ttu-id="968b5-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="968b5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="968b5-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="968b5-115">-Name</span></span>
<span data-ttu-id="968b5-116">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="968b5-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="968b5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="968b5-117">-PassThru</span></span>
<span data-ttu-id="968b5-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="968b5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="968b5-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="968b5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="968b5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="968b5-120">-ResourceGroupName</span></span>
<span data-ttu-id="968b5-121">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="968b5-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="968b5-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="968b5-122">-Confirm</span></span>
<span data-ttu-id="968b5-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="968b5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="968b5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="968b5-124">-WhatIf</span></span>
<span data-ttu-id="968b5-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="968b5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="968b5-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="968b5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="968b5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968b5-127">CommonParameters</span></span>
<span data-ttu-id="968b5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="968b5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968b5-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="968b5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968b5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="968b5-130">INPUTS</span></span>

### <span data-ttu-id="968b5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="968b5-131">System.String</span></span>

## <span data-ttu-id="968b5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="968b5-132">OUTPUTS</span></span>

### <span data-ttu-id="968b5-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="968b5-133">System.Boolean</span></span>

## <span data-ttu-id="968b5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="968b5-134">NOTES</span></span>

## <span data-ttu-id="968b5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="968b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="968b5-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="968b5-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="968b5-137">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="968b5-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="968b5-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="968b5-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="968b5-139">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="968b5-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


