---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 0e1182843ee57809fe3c6a0ed1c7f516678fc1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576545"
---
# <span data-ttu-id="d7f85-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d7f85-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d7f85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7f85-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f85-103">Hämtar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7f85-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7f85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7f85-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7f85-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f85-106">Cmdleten **Get-AzureRmDataLakeStoreItemAclEntry** hämtar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7f85-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d7f85-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7f85-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f85-108">Exempel 1: Hämta ACL för en mapp</span><span class="sxs-lookup"><span data-stu-id="d7f85-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="d7f85-109">Det här kommandot får ACL för rot katalogen för det angivna data Lake Store-kontot</span><span class="sxs-lookup"><span data-stu-id="d7f85-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="d7f85-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7f85-110">PARAMETERS</span></span>

### <span data-ttu-id="d7f85-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d7f85-111">-Account</span></span>
<span data-ttu-id="d7f85-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="d7f85-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f85-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f85-113">-DefaultProfile</span></span>
<span data-ttu-id="d7f85-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f85-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f85-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d7f85-115">-Path</span></span>
<span data-ttu-id="d7f85-116">Anger sökvägen till data Lake Store för det objekt som den här cmdleten får en ACE för och som börjar med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="d7f85-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f85-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f85-117">CommonParameters</span></span>
<span data-ttu-id="d7f85-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f85-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f85-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f85-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f85-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7f85-120">INPUTS</span></span>

### <span data-ttu-id="d7f85-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7f85-121">None</span></span>
<span data-ttu-id="d7f85-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d7f85-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7f85-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7f85-123">OUTPUTS</span></span>

### <span data-ttu-id="d7f85-124">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="d7f85-124">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="d7f85-125">Listan med ACL-poster för den angivna mappen eller filen.</span><span class="sxs-lookup"><span data-stu-id="d7f85-125">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="d7f85-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7f85-126">NOTES</span></span>

## <span data-ttu-id="d7f85-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7f85-127">RELATED LINKS</span></span>

[<span data-ttu-id="d7f85-128">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d7f85-128">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="d7f85-129">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d7f85-129">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


