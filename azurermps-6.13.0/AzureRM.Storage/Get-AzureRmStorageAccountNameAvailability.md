---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 402e3fdfe108486cd356af8a20ea06793f533937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583400"
---
# <span data-ttu-id="cd59f-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cd59f-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="cd59f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd59f-102">SYNOPSIS</span></span>
<span data-ttu-id="cd59f-103">Kontrollerar tillgänglighet för ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="cd59f-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd59f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd59f-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd59f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd59f-105">DESCRIPTION</span></span>
<span data-ttu-id="cd59f-106">Cmdleten **Get-AzureRmStorageAccountNameAvailability** kontrollerar om namnet på ett Azure Storage-konto är giltigt och tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="cd59f-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="cd59f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd59f-107">EXAMPLES</span></span>

### <span data-ttu-id="cd59f-108">Exempel 1: kontrol lera tillgänglighet för ett lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="cd59f-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="cd59f-109">Det här kommandot kontrollerar tillgängligheten för namnet ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="cd59f-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="cd59f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd59f-110">PARAMETERS</span></span>

### <span data-ttu-id="cd59f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd59f-111">-DefaultProfile</span></span>
<span data-ttu-id="cd59f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd59f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd59f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd59f-113">-Name</span></span>
<span data-ttu-id="cd59f-114">Anger namnet på det lagrings konto som denna cmdlet kontrollerar.</span><span class="sxs-lookup"><span data-stu-id="cd59f-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="cd59f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd59f-115">CommonParameters</span></span>
<span data-ttu-id="cd59f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd59f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd59f-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd59f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd59f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd59f-118">INPUTS</span></span>

### <span data-ttu-id="cd59f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="cd59f-119">System.String</span></span>

## <span data-ttu-id="cd59f-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd59f-120">OUTPUTS</span></span>

### <span data-ttu-id="cd59f-121">Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="cd59f-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="cd59f-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd59f-122">NOTES</span></span>

## <span data-ttu-id="cd59f-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd59f-123">RELATED LINKS</span></span>

[<span data-ttu-id="cd59f-124">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="cd59f-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


