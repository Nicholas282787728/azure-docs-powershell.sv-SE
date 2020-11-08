---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: fadeb5c9fdee8028364f8e65ccd7e7e70a20572b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920943"
---
# <span data-ttu-id="8911f-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8911f-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="8911f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8911f-102">SYNOPSIS</span></span>
<span data-ttu-id="8911f-103">Tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="8911f-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="8911f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8911f-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8911f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8911f-105">DESCRIPTION</span></span>
<span data-ttu-id="8911f-106">Cmdleten **Remove-AzStorageAccount** tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="8911f-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="8911f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8911f-107">EXAMPLES</span></span>

### <span data-ttu-id="8911f-108">Exempel 1: ta bort ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="8911f-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="8911f-109">Det här kommandot tar bort det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="8911f-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="8911f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8911f-110">PARAMETERS</span></span>

### <span data-ttu-id="8911f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8911f-111">-AsJob</span></span>
<span data-ttu-id="8911f-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8911f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8911f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8911f-113">-DefaultProfile</span></span>
<span data-ttu-id="8911f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8911f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8911f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8911f-115">-Force</span></span>
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

### <span data-ttu-id="8911f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="8911f-116">-Name</span></span>
<span data-ttu-id="8911f-117">Anger namnet på det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8911f-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8911f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8911f-118">-ResourceGroupName</span></span>
<span data-ttu-id="8911f-119">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8911f-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="8911f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8911f-120">-Confirm</span></span>
<span data-ttu-id="8911f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8911f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8911f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8911f-122">-WhatIf</span></span>
<span data-ttu-id="8911f-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8911f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8911f-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8911f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8911f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8911f-125">CommonParameters</span></span>
<span data-ttu-id="8911f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8911f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8911f-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8911f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8911f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8911f-128">INPUTS</span></span>

### <span data-ttu-id="8911f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8911f-129">System.String</span></span>

## <span data-ttu-id="8911f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8911f-130">OUTPUTS</span></span>

### <span data-ttu-id="8911f-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="8911f-131">System.Void</span></span>

## <span data-ttu-id="8911f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8911f-132">NOTES</span></span>

## <span data-ttu-id="8911f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8911f-133">RELATED LINKS</span></span>

[<span data-ttu-id="8911f-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8911f-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="8911f-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8911f-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="8911f-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8911f-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

