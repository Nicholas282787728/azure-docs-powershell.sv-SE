---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 47d10b02cbe019571a94ffcc1384340daff15c31
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755077"
---
# <span data-ttu-id="4d36c-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4d36c-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="4d36c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d36c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d36c-103">Tar bort ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4d36c-103">Removes a Batch account.</span></span>

## <span data-ttu-id="4d36c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d36c-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d36c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d36c-105">DESCRIPTION</span></span>
<span data-ttu-id="4d36c-106">Cmdleten **Remove-AzBatchAccount** tar bort ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="4d36c-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="4d36c-107">Denna cmdlet frågar dig innan det tar bort ett konto, om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="4d36c-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="4d36c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d36c-108">EXAMPLES</span></span>

### <span data-ttu-id="4d36c-109">Exempel 1: ta bort ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="4d36c-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="4d36c-110">Det här kommandot tar bort batch-kontot som heter pfuller.</span><span class="sxs-lookup"><span data-stu-id="4d36c-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="4d36c-111">Det här kommandot ber dig bekräfta innan kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="4d36c-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="4d36c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d36c-112">PARAMETERS</span></span>

### <span data-ttu-id="4d36c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d36c-113">-AccountName</span></span>
<span data-ttu-id="4d36c-114">Anger namnet på den Batch-konto som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4d36c-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4d36c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d36c-115">-DefaultProfile</span></span>
<span data-ttu-id="4d36c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d36c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d36c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d36c-117">-Force</span></span>
<span data-ttu-id="4d36c-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4d36c-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d36c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d36c-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d36c-120">Anger resurs gruppen för det konto som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4d36c-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4d36c-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d36c-121">-Confirm</span></span>
<span data-ttu-id="4d36c-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d36c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d36c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d36c-123">-WhatIf</span></span>
<span data-ttu-id="4d36c-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d36c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d36c-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d36c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d36c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d36c-126">CommonParameters</span></span>
<span data-ttu-id="4d36c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d36c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d36c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d36c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d36c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d36c-129">INPUTS</span></span>

### <span data-ttu-id="4d36c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4d36c-130">System.String</span></span>

## <span data-ttu-id="4d36c-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d36c-131">OUTPUTS</span></span>

### <span data-ttu-id="4d36c-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="4d36c-132">System.Void</span></span>

## <span data-ttu-id="4d36c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d36c-133">NOTES</span></span>

## <span data-ttu-id="4d36c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d36c-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d36c-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4d36c-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="4d36c-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4d36c-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="4d36c-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4d36c-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="4d36c-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4d36c-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


