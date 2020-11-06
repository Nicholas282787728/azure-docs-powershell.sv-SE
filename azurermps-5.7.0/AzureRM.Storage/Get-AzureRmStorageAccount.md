---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574140"
---
# <span data-ttu-id="5fea0-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fea0-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="5fea0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fea0-102">SYNOPSIS</span></span>
<span data-ttu-id="5fea0-103">Hämtar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5fea0-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fea0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fea0-104">SYNTAX</span></span>

### <span data-ttu-id="5fea0-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fea0-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="5fea0-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fea0-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="5fea0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fea0-107">DESCRIPTION</span></span>
<span data-ttu-id="5fea0-108">Cmdleten **Get-AzureRmStorageAccount** hämtar ett angivet lagrings konto eller alla lagrings konton i en resurs grupp eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5fea0-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="5fea0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fea0-109">EXAMPLES</span></span>

### <span data-ttu-id="5fea0-110">Exempel 1: skaffa ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5fea0-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="5fea0-111">Det här kommandot hämtar det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5fea0-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="5fea0-112">Exempel 2: Hämta alla lagrings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="5fea0-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="5fea0-113">Det här kommandot får alla lagrings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5fea0-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="5fea0-114">Exempel 3: Hämta alla lagrings konton i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="5fea0-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="5fea0-115">Det här kommandot får alla lagrings konton i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5fea0-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="5fea0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fea0-116">PARAMETERS</span></span>

### <span data-ttu-id="5fea0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fea0-117">-Name</span></span>
<span data-ttu-id="5fea0-118">Anger namnet på det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5fea0-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fea0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fea0-119">-ResourceGroupName</span></span>
<span data-ttu-id="5fea0-120">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="5fea0-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fea0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fea0-121">CommonParameters</span></span>
<span data-ttu-id="5fea0-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fea0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fea0-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fea0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fea0-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fea0-124">INPUTS</span></span>

### <span data-ttu-id="5fea0-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="5fea0-125">None</span></span>
<span data-ttu-id="5fea0-126">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5fea0-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fea0-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fea0-127">OUTPUTS</span></span>

## <span data-ttu-id="5fea0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fea0-128">NOTES</span></span>

## <span data-ttu-id="5fea0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fea0-129">RELATED LINKS</span></span>

[<span data-ttu-id="5fea0-130">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fea0-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="5fea0-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fea0-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="5fea0-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5fea0-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
