---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3528d66c635de78347647f0d1e451dc0b173a641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574026"
---
# <span data-ttu-id="07a34-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="07a34-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="07a34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07a34-102">SYNOPSIS</span></span>
<span data-ttu-id="07a34-103">Tar bort ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="07a34-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07a34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07a34-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07a34-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07a34-105">DESCRIPTION</span></span>
<span data-ttu-id="07a34-106">Cmdleten **Remove-AzureRmBatchAccount** tar bort ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="07a34-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="07a34-107">Denna cmdlet frågar dig innan det tar bort ett konto, om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="07a34-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="07a34-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07a34-108">EXAMPLES</span></span>

### <span data-ttu-id="07a34-109">Exempel 1: ta bort ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="07a34-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="07a34-110">Det här kommandot tar bort batch-kontot som heter pfuller.</span><span class="sxs-lookup"><span data-stu-id="07a34-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="07a34-111">Det här kommandot ber dig bekräfta innan kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="07a34-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="07a34-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07a34-112">PARAMETERS</span></span>

### <span data-ttu-id="07a34-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="07a34-113">-AccountName</span></span>
<span data-ttu-id="07a34-114">Anger namnet på den Batch-konto som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="07a34-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07a34-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07a34-115">-DefaultProfile</span></span>
<span data-ttu-id="07a34-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07a34-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07a34-117">-Force</span><span class="sxs-lookup"><span data-stu-id="07a34-117">-Force</span></span>
<span data-ttu-id="07a34-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="07a34-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07a34-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07a34-119">-ResourceGroupName</span></span>
<span data-ttu-id="07a34-120">Anger resurs gruppen för det konto som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="07a34-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="07a34-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07a34-121">-Confirm</span></span>
<span data-ttu-id="07a34-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07a34-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07a34-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07a34-123">-WhatIf</span></span>
<span data-ttu-id="07a34-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07a34-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07a34-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07a34-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07a34-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07a34-126">CommonParameters</span></span>
<span data-ttu-id="07a34-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07a34-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07a34-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07a34-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07a34-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07a34-129">INPUTS</span></span>

### <span data-ttu-id="07a34-130">System. String</span><span class="sxs-lookup"><span data-stu-id="07a34-130">System.String</span></span>

## <span data-ttu-id="07a34-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07a34-131">OUTPUTS</span></span>

### <span data-ttu-id="07a34-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="07a34-132">System.Void</span></span>

## <span data-ttu-id="07a34-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07a34-133">NOTES</span></span>

## <span data-ttu-id="07a34-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07a34-134">RELATED LINKS</span></span>

[<span data-ttu-id="07a34-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="07a34-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="07a34-136">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="07a34-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="07a34-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="07a34-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="07a34-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="07a34-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


