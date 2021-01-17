---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402539"
---
# <span data-ttu-id="715a0-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="715a0-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="715a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="715a0-102">SYNOPSIS</span></span>
<span data-ttu-id="715a0-103">Hämtar en post i ACL för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="715a0-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="715a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="715a0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="715a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="715a0-105">DESCRIPTION</span></span>
<span data-ttu-id="715a0-106">Cmdleten **Get-AzDataLakeStoreItemAclEntry** hämtar en post (ACE) i åtkomst kontrol listan (ACL) för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="715a0-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="715a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="715a0-107">EXAMPLES</span></span>

### <span data-ttu-id="715a0-108">Exempel 1: Hämta ACL för en mapp</span><span class="sxs-lookup"><span data-stu-id="715a0-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="715a0-109">Det här kommandot får ACL för rot katalogen för det angivna data Lake Store-kontot</span><span class="sxs-lookup"><span data-stu-id="715a0-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="715a0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="715a0-110">PARAMETERS</span></span>

### <span data-ttu-id="715a0-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="715a0-111">-Account</span></span>
<span data-ttu-id="715a0-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="715a0-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="715a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715a0-113">-DefaultProfile</span></span>
<span data-ttu-id="715a0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="715a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="715a0-115">-Path</span><span class="sxs-lookup"><span data-stu-id="715a0-115">-Path</span></span>
<span data-ttu-id="715a0-116">Anger sökvägen till data Lake Store för det objekt som den här cmdleten får en ACE för och som börjar med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="715a0-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="715a0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715a0-117">CommonParameters</span></span>
<span data-ttu-id="715a0-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715a0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715a0-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="715a0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715a0-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="715a0-120">INPUTS</span></span>

### <span data-ttu-id="715a0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="715a0-121">System.String</span></span>

### <span data-ttu-id="715a0-122">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="715a0-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="715a0-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="715a0-123">OUTPUTS</span></span>

### <span data-ttu-id="715a0-124">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="715a0-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="715a0-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="715a0-125">NOTES</span></span>

## <span data-ttu-id="715a0-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="715a0-126">RELATED LINKS</span></span>

[<span data-ttu-id="715a0-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="715a0-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="715a0-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="715a0-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


