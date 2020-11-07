---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 03e77346c14e095a11720b8cdaf930eaaa397f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920856"
---
# <span data-ttu-id="fcdfa-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fcdfa-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="fcdfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fcdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdfa-103">Hämtar tjänst egenskaper för Azure Storage BLOB-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="fcdfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fcdfa-104">SYNTAX</span></span>

### <span data-ttu-id="fcdfa-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="fcdfa-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcdfa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fcdfa-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fcdfa-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="fcdfa-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcdfa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fcdfa-108">DESCRIPTION</span></span>
<span data-ttu-id="fcdfa-109">Cmdleten **Get-AzStorageBlobServiceProperty** hämtar tjänst egenskaperna för Azure Storage BLOB-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="fcdfa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fcdfa-110">EXAMPLES</span></span>

### <span data-ttu-id="fcdfa-111">Exempel 1: skaffa Azure Storage BLOB Services-egenskap för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="fcdfa-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="fcdfa-112">Det här kommandot får egenskapen blobb för ett angivet lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="fcdfa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fcdfa-113">PARAMETERS</span></span>

### <span data-ttu-id="fcdfa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdfa-114">-DefaultProfile</span></span>
<span data-ttu-id="fcdfa-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcdfa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcdfa-116">-ResourceGroupName</span></span>
<span data-ttu-id="fcdfa-117">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdfa-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcdfa-118">-ResourceId</span></span>
<span data-ttu-id="fcdfa-119">Egenskaper för BLOB service-resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcdfa-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdfa-120">-StorageAccount</span></span>
<span data-ttu-id="fcdfa-121">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="fcdfa-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcdfa-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fcdfa-122">-StorageAccountName</span></span>
<span data-ttu-id="fcdfa-123">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdfa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdfa-124">CommonParameters</span></span>
<span data-ttu-id="fcdfa-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcdfa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdfa-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcdfa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdfa-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fcdfa-127">INPUTS</span></span>

### <span data-ttu-id="fcdfa-128">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcdfa-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fcdfa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fcdfa-129">System.String</span></span>

## <span data-ttu-id="fcdfa-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fcdfa-130">OUTPUTS</span></span>

### <span data-ttu-id="fcdfa-131">Microsoft. Azure. commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="fcdfa-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="fcdfa-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fcdfa-132">NOTES</span></span>

## <span data-ttu-id="fcdfa-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fcdfa-133">RELATED LINKS</span></span>
