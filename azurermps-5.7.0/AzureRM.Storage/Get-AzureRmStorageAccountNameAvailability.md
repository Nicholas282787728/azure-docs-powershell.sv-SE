---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755367"
---
# <span data-ttu-id="1c1af-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1c1af-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="1c1af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c1af-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1af-103">Kontrollerar tillgänglighet för ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="1c1af-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c1af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c1af-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="1c1af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c1af-105">DESCRIPTION</span></span>
<span data-ttu-id="1c1af-106">Cmdleten **Get-AzureRmStorageAccountNameAvailability** kontrollerar om namnet på ett Azure Storage-konto är giltigt och tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="1c1af-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="1c1af-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c1af-107">EXAMPLES</span></span>

### <span data-ttu-id="1c1af-108">Exempel 1: kontrol lera tillgänglighet för ett lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="1c1af-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="1c1af-109">Det här kommandot kontrollerar tillgängligheten för namnet ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="1c1af-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="1c1af-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c1af-110">PARAMETERS</span></span>

### <span data-ttu-id="1c1af-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c1af-111">-Name</span></span>
<span data-ttu-id="1c1af-112">Anger namnet på det lagrings konto som denna cmdlet kontrollerar.</span><span class="sxs-lookup"><span data-stu-id="1c1af-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1af-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1af-113">CommonParameters</span></span>
<span data-ttu-id="1c1af-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c1af-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1af-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c1af-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1af-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c1af-116">INPUTS</span></span>

### <span data-ttu-id="1c1af-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="1c1af-117">None</span></span>
<span data-ttu-id="1c1af-118">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1c1af-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c1af-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c1af-119">OUTPUTS</span></span>

## <span data-ttu-id="1c1af-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c1af-120">NOTES</span></span>

## <span data-ttu-id="1c1af-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c1af-121">RELATED LINKS</span></span>

[<span data-ttu-id="1c1af-122">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1c1af-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)
