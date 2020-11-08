---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088225"
---
# <span data-ttu-id="b9367-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9367-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="b9367-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9367-102">SYNOPSIS</span></span>
<span data-ttu-id="b9367-103">Hämtar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b9367-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b9367-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9367-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9367-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9367-105">DESCRIPTION</span></span>
<span data-ttu-id="b9367-106">Cmdleten **Get-AzDataLakeStoreItemAclEntry** hämtar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b9367-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b9367-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9367-107">EXAMPLES</span></span>

### <span data-ttu-id="b9367-108">Exempel 1: Hämta ACL för en mapp</span><span class="sxs-lookup"><span data-stu-id="b9367-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="b9367-109">Det här kommandot får ACL för rot katalogen för det angivna data Lake Store-kontot</span><span class="sxs-lookup"><span data-stu-id="b9367-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="b9367-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9367-110">PARAMETERS</span></span>

### <span data-ttu-id="b9367-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b9367-111">-Account</span></span>
<span data-ttu-id="b9367-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="b9367-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b9367-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9367-113">-DefaultProfile</span></span>
<span data-ttu-id="b9367-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9367-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9367-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b9367-115">-Path</span></span>
<span data-ttu-id="b9367-116">Anger sökvägen till data Lake Store för det objekt som den här cmdleten får en ACE för och som börjar med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="b9367-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b9367-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9367-117">CommonParameters</span></span>
<span data-ttu-id="b9367-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9367-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9367-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9367-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9367-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9367-120">INPUTS</span></span>

### <span data-ttu-id="b9367-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b9367-121">System.String</span></span>

### <span data-ttu-id="b9367-122">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b9367-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="b9367-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9367-123">OUTPUTS</span></span>

### <span data-ttu-id="b9367-124">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="b9367-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="b9367-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9367-125">NOTES</span></span>

## <span data-ttu-id="b9367-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9367-126">RELATED LINKS</span></span>

[<span data-ttu-id="b9367-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9367-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="b9367-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b9367-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


