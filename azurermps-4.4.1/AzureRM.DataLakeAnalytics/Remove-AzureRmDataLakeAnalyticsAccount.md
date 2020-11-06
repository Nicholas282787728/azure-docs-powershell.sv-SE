---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 23f1ba9185b2a33c910afb0fc7ff0deb2a1cbf5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574690"
---
# <span data-ttu-id="fc9e7-101">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fc9e7-101">Remove-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="fc9e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9e7-103">Tar bort ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-103">Deletes a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc9e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc9e7-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc9e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="fc9e7-106">Cmdleten **Remove-AzureRmDataLakeAnalyticsAccount** tar bort ett Azure Data Lake Analytics-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-106">The **Remove-AzureRmDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="fc9e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc9e7-107">EXAMPLES</span></span>

### <span data-ttu-id="fc9e7-108">Exempel 1: ta bort ett konto</span><span class="sxs-lookup"><span data-stu-id="fc9e7-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="fc9e7-109">Detta kommando tar bort det angivna data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="fc9e7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc9e7-110">PARAMETERS</span></span>

### <span data-ttu-id="fc9e7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fc9e7-111">-Force</span></span>
<span data-ttu-id="fc9e7-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc9e7-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc9e7-113">-Name</span></span>
<span data-ttu-id="fc9e7-114">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="fc9e7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc9e7-115">-PassThru</span></span>
<span data-ttu-id="fc9e7-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc9e7-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc9e7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc9e7-118">-ResourceGroupName</span></span>
<span data-ttu-id="fc9e7-119">Anger namnet på resurs gruppen för data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="fc9e7-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fc9e7-120">-Confirm</span></span>
<span data-ttu-id="fc9e7-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc9e7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc9e7-122">-WhatIf</span></span>
<span data-ttu-id="fc9e7-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc9e7-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc9e7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc9e7-125">-DefaultProfile</span></span>
<span data-ttu-id="fc9e7-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc9e7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9e7-127">CommonParameters</span></span>
<span data-ttu-id="fc9e7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9e7-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc9e7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9e7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc9e7-130">INPUTS</span></span>

## <span data-ttu-id="fc9e7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc9e7-131">OUTPUTS</span></span>

### <span data-ttu-id="fc9e7-132">bool</span><span class="sxs-lookup"><span data-stu-id="fc9e7-132">bool</span></span>
<span data-ttu-id="fc9e7-133">Om PassThru anges returneras sant när åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="fc9e7-133">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="fc9e7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc9e7-134">NOTES</span></span>

## <span data-ttu-id="fc9e7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc9e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="fc9e7-136">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fc9e7-136">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fc9e7-137">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fc9e7-137">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fc9e7-138">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fc9e7-138">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="fc9e7-139">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="fc9e7-139">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


