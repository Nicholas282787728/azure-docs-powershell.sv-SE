---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260324"
---
# <span data-ttu-id="0eb51-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0eb51-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="0eb51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0eb51-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb51-103">Tar bort ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="0eb51-103">Removes a Batch account.</span></span>

## <span data-ttu-id="0eb51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0eb51-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb51-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0eb51-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb51-106">Cmdleten **Remove-AzBatchAccount** tar bort ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="0eb51-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="0eb51-107">Denna cmdlet frågar dig innan det tar bort ett konto, om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="0eb51-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="0eb51-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0eb51-108">EXAMPLES</span></span>

### <span data-ttu-id="0eb51-109">Exempel 1: ta bort ett batch-konto</span><span class="sxs-lookup"><span data-stu-id="0eb51-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="0eb51-110">Det här kommandot tar bort batch-kontot som heter pfuller.</span><span class="sxs-lookup"><span data-stu-id="0eb51-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="0eb51-111">Det här kommandot ber dig bekräfta innan kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="0eb51-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="0eb51-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0eb51-112">PARAMETERS</span></span>

### <span data-ttu-id="0eb51-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0eb51-113">-AccountName</span></span>
<span data-ttu-id="0eb51-114">Anger namnet på den Batch-konto som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0eb51-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0eb51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb51-115">-DefaultProfile</span></span>
<span data-ttu-id="0eb51-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb51-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb51-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0eb51-117">-Force</span></span>
<span data-ttu-id="0eb51-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0eb51-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0eb51-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb51-119">-ResourceGroupName</span></span>
<span data-ttu-id="0eb51-120">Anger resurs gruppen för det konto som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0eb51-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0eb51-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0eb51-121">-Confirm</span></span>
<span data-ttu-id="0eb51-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0eb51-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb51-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb51-123">-WhatIf</span></span>
<span data-ttu-id="0eb51-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0eb51-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb51-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0eb51-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb51-126">CommonParameters</span></span>
<span data-ttu-id="0eb51-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb51-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eb51-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb51-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0eb51-129">INPUTS</span></span>

### <span data-ttu-id="0eb51-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb51-130">System.String</span></span>

## <span data-ttu-id="0eb51-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0eb51-131">OUTPUTS</span></span>

### <span data-ttu-id="0eb51-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="0eb51-132">System.Void</span></span>

## <span data-ttu-id="0eb51-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0eb51-133">NOTES</span></span>

## <span data-ttu-id="0eb51-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0eb51-134">RELATED LINKS</span></span>

[<span data-ttu-id="0eb51-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0eb51-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="0eb51-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0eb51-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="0eb51-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0eb51-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="0eb51-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0eb51-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
