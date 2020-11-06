---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: 9c512c1993700e1bbdab4d5c0d52a1aa2ceeafb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584839"
---
# <span data-ttu-id="36efe-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36efe-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="36efe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36efe-102">SYNOPSIS</span></span>
<span data-ttu-id="36efe-103">Tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="36efe-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36efe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36efe-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36efe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36efe-105">DESCRIPTION</span></span>
<span data-ttu-id="36efe-106">Cmdleten **Remove-AzureRmStorageAccount** tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="36efe-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="36efe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36efe-107">EXAMPLES</span></span>

### <span data-ttu-id="36efe-108">Exempel 1: ta bort ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="36efe-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="36efe-109">Det här kommandot tar bort det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="36efe-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="36efe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36efe-110">PARAMETERS</span></span>

### <span data-ttu-id="36efe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36efe-111">-AsJob</span></span>
<span data-ttu-id="36efe-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="36efe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36efe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36efe-113">-DefaultProfile</span></span>
<span data-ttu-id="36efe-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36efe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36efe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="36efe-115">-Force</span></span>
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

### <span data-ttu-id="36efe-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="36efe-116">-Name</span></span>
<span data-ttu-id="36efe-117">Anger namnet på det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="36efe-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="36efe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36efe-118">-ResourceGroupName</span></span>
<span data-ttu-id="36efe-119">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="36efe-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="36efe-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36efe-120">-Confirm</span></span>
<span data-ttu-id="36efe-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36efe-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36efe-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36efe-122">-WhatIf</span></span>
<span data-ttu-id="36efe-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36efe-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36efe-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36efe-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36efe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36efe-125">CommonParameters</span></span>
<span data-ttu-id="36efe-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36efe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36efe-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36efe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36efe-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36efe-128">INPUTS</span></span>

### <span data-ttu-id="36efe-129">System. String</span><span class="sxs-lookup"><span data-stu-id="36efe-129">System.String</span></span>

## <span data-ttu-id="36efe-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36efe-130">OUTPUTS</span></span>

### <span data-ttu-id="36efe-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="36efe-131">System.Void</span></span>

## <span data-ttu-id="36efe-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36efe-132">NOTES</span></span>

## <span data-ttu-id="36efe-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36efe-133">RELATED LINKS</span></span>

[<span data-ttu-id="36efe-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36efe-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="36efe-135">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36efe-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="36efe-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36efe-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


