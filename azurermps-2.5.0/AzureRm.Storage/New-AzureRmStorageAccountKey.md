---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: 7ea3847c011582d9be809f030a638b09b6cf9532
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928641"
---
# <span data-ttu-id="7acfa-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7acfa-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="7acfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7acfa-102">SYNOPSIS</span></span>
<span data-ttu-id="7acfa-103">Återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="7acfa-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7acfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7acfa-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7acfa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7acfa-105">DESCRIPTION</span></span>
<span data-ttu-id="7acfa-106">Cmdleten **New-AzureRmStorageAccountKey** återskapar en lagrings nyckeln för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="7acfa-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="7acfa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7acfa-107">EXAMPLES</span></span>

### <span data-ttu-id="7acfa-108">Exempel 1: återskapa en lagrings nyckeln</span><span class="sxs-lookup"><span data-stu-id="7acfa-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="7acfa-109">Det här kommandot återskapar en lagrings plats för det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="7acfa-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="7acfa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7acfa-110">PARAMETERS</span></span>

### <span data-ttu-id="7acfa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acfa-111">-DefaultProfile</span></span>
<span data-ttu-id="7acfa-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7acfa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7acfa-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7acfa-113">-KeyName</span></span>
<span data-ttu-id="7acfa-114">Anger vilken nyckeln som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7acfa-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="7acfa-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7acfa-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7acfa-116">key1</span><span class="sxs-lookup"><span data-stu-id="7acfa-116">key1</span></span>
- <span data-ttu-id="7acfa-117">key2</span><span class="sxs-lookup"><span data-stu-id="7acfa-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7acfa-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7acfa-118">-Name</span></span>
<span data-ttu-id="7acfa-119">Anger namnet på det lagrings konto som du vill återskapa en lagrings plats för.</span><span class="sxs-lookup"><span data-stu-id="7acfa-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="7acfa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7acfa-120">-ResourceGroupName</span></span>
<span data-ttu-id="7acfa-121">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="7acfa-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="7acfa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acfa-122">CommonParameters</span></span>
<span data-ttu-id="7acfa-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acfa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acfa-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7acfa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acfa-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7acfa-125">INPUTS</span></span>

### <span data-ttu-id="7acfa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7acfa-126">System.String</span></span>

## <span data-ttu-id="7acfa-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7acfa-127">OUTPUTS</span></span>

### <span data-ttu-id="7acfa-128">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7acfa-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="7acfa-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7acfa-129">NOTES</span></span>

## <span data-ttu-id="7acfa-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7acfa-130">RELATED LINKS</span></span>

[<span data-ttu-id="7acfa-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7acfa-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
