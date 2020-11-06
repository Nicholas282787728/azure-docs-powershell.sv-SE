---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8ca5c33944882fde7e9bad2411df5f41dbe5f788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576679"
---
# <span data-ttu-id="1fb02-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="1fb02-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="1fb02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1fb02-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb02-103">Kontrollerar tillgänglighet för ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="1fb02-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1fb02-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb02-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1fb02-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb02-106">Cmdleten **Get-AzureRmStorageAccountNameAvailability** kontrollerar om namnet på ett Azure Storage-konto är giltigt och tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="1fb02-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="1fb02-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1fb02-107">EXAMPLES</span></span>

### <span data-ttu-id="1fb02-108">Exempel 1: kontrol lera tillgänglighet för ett lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="1fb02-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="1fb02-109">Det här kommandot kontrollerar tillgängligheten för namnet ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="1fb02-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="1fb02-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1fb02-110">PARAMETERS</span></span>

### <span data-ttu-id="1fb02-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="1fb02-111">-Name</span></span>
<span data-ttu-id="1fb02-112">Anger namnet på det lagrings konto som denna cmdlet kontrollerar.</span><span class="sxs-lookup"><span data-stu-id="1fb02-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="1fb02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb02-113">-DefaultProfile</span></span>
<span data-ttu-id="1fb02-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fb02-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb02-115">CommonParameters</span></span>
<span data-ttu-id="1fb02-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb02-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb02-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb02-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb02-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1fb02-118">INPUTS</span></span>

## <span data-ttu-id="1fb02-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1fb02-119">OUTPUTS</span></span>

## <span data-ttu-id="1fb02-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1fb02-120">NOTES</span></span>

## <span data-ttu-id="1fb02-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1fb02-121">RELATED LINKS</span></span>

[<span data-ttu-id="1fb02-122">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="1fb02-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


