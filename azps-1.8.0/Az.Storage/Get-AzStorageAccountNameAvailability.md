---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 60e30de4d6d55007ec659a267b1d450ac1cfeff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746406"
---
# <span data-ttu-id="fba64-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="fba64-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="fba64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fba64-102">SYNOPSIS</span></span>
<span data-ttu-id="fba64-103">Kontrollerar tillgänglighet för ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="fba64-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="fba64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fba64-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fba64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fba64-105">DESCRIPTION</span></span>
<span data-ttu-id="fba64-106">Cmdleten **Get-AzStorageAccountNameAvailability** kontrollerar om namnet på ett Azure Storage-konto är giltigt och tillgängligt för användning.</span><span class="sxs-lookup"><span data-stu-id="fba64-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="fba64-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fba64-107">EXAMPLES</span></span>

### <span data-ttu-id="fba64-108">Exempel 1: kontrol lera tillgänglighet för ett lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="fba64-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="fba64-109">Det här kommandot kontrollerar tillgängligheten för namnet ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="fba64-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="fba64-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fba64-110">PARAMETERS</span></span>

### <span data-ttu-id="fba64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba64-111">-DefaultProfile</span></span>
<span data-ttu-id="fba64-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fba64-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fba64-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="fba64-113">-Name</span></span>
<span data-ttu-id="fba64-114">Anger namnet på det lagrings konto som denna cmdlet kontrollerar.</span><span class="sxs-lookup"><span data-stu-id="fba64-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="fba64-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba64-115">CommonParameters</span></span>
<span data-ttu-id="fba64-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fba64-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba64-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba64-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba64-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fba64-118">INPUTS</span></span>

### <span data-ttu-id="fba64-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fba64-119">System.String</span></span>

## <span data-ttu-id="fba64-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fba64-120">OUTPUTS</span></span>

### <span data-ttu-id="fba64-121">Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="fba64-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="fba64-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fba64-122">NOTES</span></span>

## <span data-ttu-id="fba64-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fba64-123">RELATED LINKS</span></span>

[<span data-ttu-id="fba64-124">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="fba64-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


