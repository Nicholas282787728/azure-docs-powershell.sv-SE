---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: edd03d0a5836393c20b9af2da1cd89502bd2030b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744551"
---
# <span data-ttu-id="e090b-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e090b-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e090b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e090b-102">SYNOPSIS</span></span>
<span data-ttu-id="e090b-103">Tar bort ett data Lake Store-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="e090b-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="e090b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e090b-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e090b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e090b-105">DESCRIPTION</span></span>
<span data-ttu-id="e090b-106">Cmdleten **Remove-AzDataLakeStoreAccount** tar bort ett data Lake Store-konto permanent.</span><span class="sxs-lookup"><span data-stu-id="e090b-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="e090b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e090b-107">EXAMPLES</span></span>

### <span data-ttu-id="e090b-108">Exempel 1: ta bort ett data Lake Store-konto</span><span class="sxs-lookup"><span data-stu-id="e090b-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e090b-109">Det här kommandot tar bort kontot som heter ContosoADL från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e090b-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="e090b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e090b-110">PARAMETERS</span></span>

### <span data-ttu-id="e090b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e090b-111">-DefaultProfile</span></span>
<span data-ttu-id="e090b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e090b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e090b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e090b-113">-Force</span></span>
<span data-ttu-id="e090b-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e090b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e090b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="e090b-115">-Name</span></span>
<span data-ttu-id="e090b-116">Anger namnet på kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e090b-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="e090b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e090b-117">-PassThru</span></span>
<span data-ttu-id="e090b-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e090b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e090b-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e090b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e090b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e090b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e090b-121">Anger den resurs grupp som innehåller kontot som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e090b-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="e090b-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e090b-122">-Confirm</span></span>
<span data-ttu-id="e090b-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e090b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e090b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e090b-124">-WhatIf</span></span>
<span data-ttu-id="e090b-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e090b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e090b-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e090b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e090b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e090b-127">CommonParameters</span></span>
<span data-ttu-id="e090b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e090b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e090b-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e090b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e090b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e090b-130">INPUTS</span></span>

### <span data-ttu-id="e090b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e090b-131">System.String</span></span>

## <span data-ttu-id="e090b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e090b-132">OUTPUTS</span></span>

### <span data-ttu-id="e090b-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e090b-133">System.Boolean</span></span>

## <span data-ttu-id="e090b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e090b-134">NOTES</span></span>

## <span data-ttu-id="e090b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e090b-135">RELATED LINKS</span></span>

[<span data-ttu-id="e090b-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e090b-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e090b-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e090b-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e090b-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e090b-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e090b-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e090b-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


