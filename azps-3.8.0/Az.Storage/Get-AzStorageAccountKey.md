---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: faecfdf62892faba2f7ec1241d7e02daa1e6ed12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090026"
---
# <span data-ttu-id="a0942-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a0942-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="a0942-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0942-102">SYNOPSIS</span></span>
<span data-ttu-id="a0942-103">Hämtar åtkomst nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="a0942-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="a0942-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0942-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0942-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0942-105">DESCRIPTION</span></span>
<span data-ttu-id="a0942-106">Cmdleten **Get-AzStorageAccountKey** hämtar åtkomst nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="a0942-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="a0942-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0942-107">EXAMPLES</span></span>

### <span data-ttu-id="a0942-108">Exempel 1: Hämta snabb tangenterna för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="a0942-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="a0942-109">Det här kommandot får nycklarna för det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="a0942-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="a0942-110">Exempel 2: Hämta en specifik åtkomst för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="a0942-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="a0942-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0942-111">PARAMETERS</span></span>

### <span data-ttu-id="a0942-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0942-112">-DefaultProfile</span></span>
<span data-ttu-id="a0942-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0942-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0942-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0942-114">-Name</span></span>
<span data-ttu-id="a0942-115">Anger namnet på det lagrings konto som den här cmdleten får nycklar för.</span><span class="sxs-lookup"><span data-stu-id="a0942-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="a0942-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0942-116">-ResourceGroupName</span></span>
<span data-ttu-id="a0942-117">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="a0942-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="a0942-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0942-118">CommonParameters</span></span>
<span data-ttu-id="a0942-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0942-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0942-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0942-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0942-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0942-121">INPUTS</span></span>

### <span data-ttu-id="a0942-122">System. String</span><span class="sxs-lookup"><span data-stu-id="a0942-122">System.String</span></span>

## <span data-ttu-id="a0942-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0942-123">OUTPUTS</span></span>

### <span data-ttu-id="a0942-124">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a0942-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="a0942-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0942-125">NOTES</span></span>

## <span data-ttu-id="a0942-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0942-126">RELATED LINKS</span></span>

[<span data-ttu-id="a0942-127">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a0942-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


