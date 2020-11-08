---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccount.md
ms.openlocfilehash: e92bdaae728031ba38fc1326ac2abb29aac86c59
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092395"
---
# <span data-ttu-id="bcc29-101">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcc29-101">Remove-AzStorageAccount</span></span>

## <span data-ttu-id="bcc29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bcc29-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc29-103">Tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc29-103">Removes a Storage account from Azure.</span></span>

## <span data-ttu-id="bcc29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bcc29-104">SYNTAX</span></span>

```
Remove-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc29-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bcc29-105">DESCRIPTION</span></span>
<span data-ttu-id="bcc29-106">Cmdleten **Remove-AzStorageAccount** tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc29-106">The **Remove-AzStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="bcc29-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bcc29-107">EXAMPLES</span></span>

### <span data-ttu-id="bcc29-108">Exempel 1: ta bort ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="bcc29-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="bcc29-109">Det här kommandot tar bort det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="bcc29-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="bcc29-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bcc29-110">PARAMETERS</span></span>

### <span data-ttu-id="bcc29-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcc29-111">-AsJob</span></span>
<span data-ttu-id="bcc29-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bcc29-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcc29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc29-113">-DefaultProfile</span></span>
<span data-ttu-id="bcc29-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bcc29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc29-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bcc29-115">-Force</span></span>
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

### <span data-ttu-id="bcc29-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="bcc29-116">-Name</span></span>
<span data-ttu-id="bcc29-117">Anger namnet på det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="bcc29-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="bcc29-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc29-118">-ResourceGroupName</span></span>
<span data-ttu-id="bcc29-119">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="bcc29-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="bcc29-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bcc29-120">-Confirm</span></span>
<span data-ttu-id="bcc29-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bcc29-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc29-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc29-122">-WhatIf</span></span>
<span data-ttu-id="bcc29-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bcc29-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcc29-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bcc29-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc29-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc29-125">CommonParameters</span></span>
<span data-ttu-id="bcc29-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc29-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc29-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc29-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc29-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bcc29-128">INPUTS</span></span>

### <span data-ttu-id="bcc29-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bcc29-129">System.String</span></span>

## <span data-ttu-id="bcc29-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bcc29-130">OUTPUTS</span></span>

### <span data-ttu-id="bcc29-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="bcc29-131">System.Void</span></span>

## <span data-ttu-id="bcc29-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bcc29-132">NOTES</span></span>

## <span data-ttu-id="bcc29-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bcc29-133">RELATED LINKS</span></span>

[<span data-ttu-id="bcc29-134">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcc29-134">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="bcc29-135">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcc29-135">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="bcc29-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcc29-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


