---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388872"
---
# <span data-ttu-id="2927b-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2927b-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="2927b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2927b-102">SYNOPSIS</span></span>
<span data-ttu-id="2927b-103">Hämtar tjänst egenskaper för Azure Storage File Services.</span><span class="sxs-lookup"><span data-stu-id="2927b-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="2927b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2927b-104">SYNTAX</span></span>

### <span data-ttu-id="2927b-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="2927b-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2927b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2927b-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2927b-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="2927b-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2927b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2927b-108">DESCRIPTION</span></span>
<span data-ttu-id="2927b-109">Cmdleten **Get-AzStorageFileServiceProperty** hämtar tjänst egenskaperna för Azure Storage File Services.</span><span class="sxs-lookup"><span data-stu-id="2927b-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="2927b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2927b-110">EXAMPLES</span></span>

### <span data-ttu-id="2927b-111">Exempel 1: Hämta Azure Storage File Services-egenskapen för ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="2927b-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="2927b-112">Det här kommandot får egenskapen fil tjänster för ett angivet lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="2927b-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="2927b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2927b-113">PARAMETERS</span></span>

### <span data-ttu-id="2927b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2927b-114">-DefaultProfile</span></span>
<span data-ttu-id="2927b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2927b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2927b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2927b-116">-ResourceGroupName</span></span>
<span data-ttu-id="2927b-117">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2927b-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="2927b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2927b-118">-ResourceId</span></span>
<span data-ttu-id="2927b-119">Ange ett resurs-ID för ett lagrings konto eller ett resurs namn för fil tjänst egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2927b-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="2927b-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2927b-120">-StorageAccount</span></span>
<span data-ttu-id="2927b-121">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="2927b-121">Storage account object</span></span>

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

### <span data-ttu-id="2927b-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2927b-122">-StorageAccountName</span></span>
<span data-ttu-id="2927b-123">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="2927b-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="2927b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2927b-124">CommonParameters</span></span>
<span data-ttu-id="2927b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2927b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2927b-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2927b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2927b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2927b-127">INPUTS</span></span>

### <span data-ttu-id="2927b-128">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2927b-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2927b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2927b-129">System.String</span></span>

## <span data-ttu-id="2927b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2927b-130">OUTPUTS</span></span>

### <span data-ttu-id="2927b-131">Microsoft. Azure. commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="2927b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="2927b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2927b-132">NOTES</span></span>

## <span data-ttu-id="2927b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2927b-133">RELATED LINKS</span></span>
