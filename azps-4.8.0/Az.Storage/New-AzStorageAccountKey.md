---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261529"
---
# <span data-ttu-id="55dfc-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="55dfc-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="55dfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="55dfc-103">Återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="55dfc-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="55dfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55dfc-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55dfc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="55dfc-106">Cmdleten **New-AzStorageAccountKey** återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="55dfc-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="55dfc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="55dfc-108">Exempel 1: återskapa en lagrings nyckeln</span><span class="sxs-lookup"><span data-stu-id="55dfc-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="55dfc-109">Det här kommandot återskapar en lagrings plats för det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="55dfc-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="55dfc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="55dfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55dfc-111">-DefaultProfile</span></span>
<span data-ttu-id="55dfc-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55dfc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55dfc-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="55dfc-113">-KeyName</span></span>
<span data-ttu-id="55dfc-114">Anger vilken nyckeln som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="55dfc-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="55dfc-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="55dfc-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55dfc-116">key1</span><span class="sxs-lookup"><span data-stu-id="55dfc-116">key1</span></span>
- <span data-ttu-id="55dfc-117">key2</span><span class="sxs-lookup"><span data-stu-id="55dfc-117">key2</span></span>
- <span data-ttu-id="55dfc-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="55dfc-118">kerb1</span></span>
- <span data-ttu-id="55dfc-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="55dfc-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55dfc-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="55dfc-120">-Name</span></span>
<span data-ttu-id="55dfc-121">Anger namnet på det lagrings konto som du vill återskapa en lagrings plats för.</span><span class="sxs-lookup"><span data-stu-id="55dfc-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="55dfc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55dfc-122">-ResourceGroupName</span></span>
<span data-ttu-id="55dfc-123">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="55dfc-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="55dfc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55dfc-124">CommonParameters</span></span>
<span data-ttu-id="55dfc-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55dfc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55dfc-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55dfc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55dfc-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55dfc-127">INPUTS</span></span>

### <span data-ttu-id="55dfc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="55dfc-128">System.String</span></span>

## <span data-ttu-id="55dfc-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55dfc-129">OUTPUTS</span></span>

### <span data-ttu-id="55dfc-130">Microsoft. Azure. Management. Storage. Models. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="55dfc-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="55dfc-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55dfc-131">NOTES</span></span>

## <span data-ttu-id="55dfc-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55dfc-132">RELATED LINKS</span></span>

[<span data-ttu-id="55dfc-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="55dfc-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
