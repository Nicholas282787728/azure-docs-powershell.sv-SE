---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756983"
---
# <span data-ttu-id="54dda-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="54dda-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="54dda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54dda-102">SYNOPSIS</span></span>
<span data-ttu-id="54dda-103">Hämtar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="54dda-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54dda-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54dda-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54dda-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54dda-105">DESCRIPTION</span></span>
<span data-ttu-id="54dda-106">Cmdleten **Get-AzureRmDataLakeStoreItemAclEntry** hämtar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="54dda-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="54dda-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54dda-107">EXAMPLES</span></span>

### <span data-ttu-id="54dda-108">Exempel 1: Hämta ACL för en mapp</span><span class="sxs-lookup"><span data-stu-id="54dda-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="54dda-109">Det här kommandot får ACL för rot katalogen för det angivna data Lake Store-kontot</span><span class="sxs-lookup"><span data-stu-id="54dda-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="54dda-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54dda-110">PARAMETERS</span></span>

### <span data-ttu-id="54dda-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="54dda-111">-Account</span></span>
<span data-ttu-id="54dda-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="54dda-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54dda-113">-Path</span><span class="sxs-lookup"><span data-stu-id="54dda-113">-Path</span></span>
<span data-ttu-id="54dda-114">Anger sökvägen till data Lake Store för det objekt som den här cmdleten får en ACE för och som börjar med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="54dda-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54dda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54dda-115">-DefaultProfile</span></span>
<span data-ttu-id="54dda-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54dda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54dda-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54dda-117">CommonParameters</span></span>
<span data-ttu-id="54dda-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54dda-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54dda-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54dda-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54dda-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54dda-120">INPUTS</span></span>

## <span data-ttu-id="54dda-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54dda-121">OUTPUTS</span></span>

### <span data-ttu-id="54dda-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="54dda-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="54dda-123">Listan med ACL-poster för den angivna mappen eller filen.</span><span class="sxs-lookup"><span data-stu-id="54dda-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="54dda-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54dda-124">NOTES</span></span>

## <span data-ttu-id="54dda-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54dda-125">RELATED LINKS</span></span>

[<span data-ttu-id="54dda-126">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="54dda-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="54dda-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="54dda-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


