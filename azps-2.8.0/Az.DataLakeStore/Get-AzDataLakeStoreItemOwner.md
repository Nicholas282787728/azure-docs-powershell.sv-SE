---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 64af120d793719d4bcd6a24cc3d480cc8f6c104f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744570"
---
# <span data-ttu-id="7c70a-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="7c70a-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="7c70a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c70a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c70a-103">Hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7c70a-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7c70a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c70a-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c70a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c70a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c70a-106">Cmdleten **Get-AzDataLakeStoreItemOwner** hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7c70a-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7c70a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c70a-107">EXAMPLES</span></span>

### <span data-ttu-id="7c70a-108">Exempel 1: Hämta ägaren till en katalog</span><span class="sxs-lookup"><span data-stu-id="7c70a-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="7c70a-109">Det här kommandot får användarens ägare till rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="7c70a-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="7c70a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c70a-110">PARAMETERS</span></span>

### <span data-ttu-id="7c70a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="7c70a-111">-Account</span></span>
<span data-ttu-id="7c70a-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="7c70a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7c70a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c70a-113">-DefaultProfile</span></span>
<span data-ttu-id="7c70a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c70a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c70a-115">-Path</span><span class="sxs-lookup"><span data-stu-id="7c70a-115">-Path</span></span>
<span data-ttu-id="7c70a-116">Anger data Lake Store-sökvägen för ett objekt, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="7c70a-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7c70a-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="7c70a-117">-Type</span></span>
<span data-ttu-id="7c70a-118">Anger typen av ägare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="7c70a-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="7c70a-119">De acceptabla värdena för denna parameter är: User och Group.</span><span class="sxs-lookup"><span data-stu-id="7c70a-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c70a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c70a-120">CommonParameters</span></span>
<span data-ttu-id="7c70a-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c70a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c70a-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c70a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c70a-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c70a-123">INPUTS</span></span>

### <span data-ttu-id="7c70a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7c70a-124">System.String</span></span>

### <span data-ttu-id="7c70a-125">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7c70a-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7c70a-126">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="7c70a-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="7c70a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c70a-127">OUTPUTS</span></span>

### <span data-ttu-id="7c70a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7c70a-128">System.String</span></span>

## <span data-ttu-id="7c70a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c70a-129">NOTES</span></span>

## <span data-ttu-id="7c70a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c70a-130">RELATED LINKS</span></span>

[<span data-ttu-id="7c70a-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="7c70a-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


