---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269578"
---
# <span data-ttu-id="ef4b8-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ef4b8-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="ef4b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4b8-103">Hämtar tjänst egenskaper för Azure Storage File Services.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="ef4b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef4b8-104">SYNTAX</span></span>

### <span data-ttu-id="ef4b8-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="ef4b8-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef4b8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ef4b8-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef4b8-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="ef4b8-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef4b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef4b8-108">DESCRIPTION</span></span>
<span data-ttu-id="ef4b8-109">Cmdleten **Get-AzStorageFileServiceProperty** hämtar tjänst egenskaperna för Azure Storage File Services.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="ef4b8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef4b8-110">EXAMPLES</span></span>

### <span data-ttu-id="ef4b8-111">Exempel 1: Hämta Azure Storage File Services-egenskapen för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ef4b8-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="ef4b8-112">Det här kommandot får egenskapen fil tjänster för ett angivet lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="ef4b8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef4b8-113">PARAMETERS</span></span>

### <span data-ttu-id="ef4b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4b8-114">-DefaultProfile</span></span>
<span data-ttu-id="ef4b8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4b8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4b8-116">-ResourceGroupName</span></span>
<span data-ttu-id="ef4b8-117">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef4b8-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef4b8-118">-ResourceId</span></span>
<span data-ttu-id="ef4b8-119">Ange ett resurs-ID för ett lagrings konto eller ett resurs namn för fil tjänst egenskaper.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4b8-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ef4b8-120">-StorageAccount</span></span>
<span data-ttu-id="ef4b8-121">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="ef4b8-121">Storage account object</span></span>

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

### <span data-ttu-id="ef4b8-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef4b8-122">-StorageAccountName</span></span>
<span data-ttu-id="ef4b8-123">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="ef4b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4b8-124">CommonParameters</span></span>
<span data-ttu-id="ef4b8-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4b8-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4b8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4b8-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef4b8-127">INPUTS</span></span>

### <span data-ttu-id="ef4b8-128">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ef4b8-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ef4b8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef4b8-129">System.String</span></span>

## <span data-ttu-id="ef4b8-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef4b8-130">OUTPUTS</span></span>

### <span data-ttu-id="ef4b8-131">Microsoft. Azure. commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="ef4b8-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="ef4b8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef4b8-132">NOTES</span></span>

## <span data-ttu-id="ef4b8-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef4b8-133">RELATED LINKS</span></span>
