---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: ba63794844420accf2e5e664a43f74b2578c780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755906"
---
# <span data-ttu-id="5c999-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c999-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="5c999-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5c999-102">SYNOPSIS</span></span>
<span data-ttu-id="5c999-103">Tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="5c999-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c999-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5c999-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c999-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5c999-105">DESCRIPTION</span></span>
<span data-ttu-id="5c999-106">Cmdleten **Remove-AzureRmStorageAccount** tar bort ett lagrings konto från Azure.</span><span class="sxs-lookup"><span data-stu-id="5c999-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="5c999-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5c999-107">EXAMPLES</span></span>

### <span data-ttu-id="5c999-108">Exempel 1: ta bort ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5c999-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="5c999-109">Det här kommandot tar bort det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5c999-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="5c999-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5c999-110">PARAMETERS</span></span>

### <span data-ttu-id="5c999-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5c999-111">-Force</span></span>
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

### <span data-ttu-id="5c999-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="5c999-112">-Name</span></span>
<span data-ttu-id="5c999-113">Anger namnet på det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5c999-113">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="5c999-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c999-114">-ResourceGroupName</span></span>
<span data-ttu-id="5c999-115">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5c999-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="5c999-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5c999-116">-Confirm</span></span>
<span data-ttu-id="5c999-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5c999-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c999-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c999-118">-WhatIf</span></span>
<span data-ttu-id="5c999-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5c999-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c999-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5c999-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c999-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c999-121">-DefaultProfile</span></span>
<span data-ttu-id="5c999-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5c999-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c999-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c999-123">CommonParameters</span></span>
<span data-ttu-id="5c999-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c999-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c999-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c999-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c999-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5c999-126">INPUTS</span></span>

## <span data-ttu-id="5c999-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5c999-127">OUTPUTS</span></span>

## <span data-ttu-id="5c999-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5c999-128">NOTES</span></span>

## <span data-ttu-id="5c999-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5c999-129">RELATED LINKS</span></span>

[<span data-ttu-id="5c999-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c999-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="5c999-131">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c999-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="5c999-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c999-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


