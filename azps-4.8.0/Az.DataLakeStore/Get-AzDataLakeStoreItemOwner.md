---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260790"
---
# <span data-ttu-id="84906-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="84906-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="84906-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84906-102">SYNOPSIS</span></span>
<span data-ttu-id="84906-103">Hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="84906-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="84906-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84906-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84906-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84906-105">DESCRIPTION</span></span>
<span data-ttu-id="84906-106">Cmdleten **Get-AzDataLakeStoreItemOwner** hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="84906-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="84906-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84906-107">EXAMPLES</span></span>

### <span data-ttu-id="84906-108">Exempel 1: Hämta ägaren till en katalog</span><span class="sxs-lookup"><span data-stu-id="84906-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="84906-109">Det här kommandot får användarens ägare till rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="84906-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="84906-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84906-110">PARAMETERS</span></span>

### <span data-ttu-id="84906-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="84906-111">-Account</span></span>
<span data-ttu-id="84906-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="84906-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="84906-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84906-113">-DefaultProfile</span></span>
<span data-ttu-id="84906-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84906-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84906-115">-Path</span><span class="sxs-lookup"><span data-stu-id="84906-115">-Path</span></span>
<span data-ttu-id="84906-116">Anger data Lake Store-sökvägen för ett objekt, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="84906-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="84906-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="84906-117">-Type</span></span>
<span data-ttu-id="84906-118">Anger typen av ägare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="84906-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="84906-119">De acceptabla värdena för denna parameter är: User och Group.</span><span class="sxs-lookup"><span data-stu-id="84906-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="84906-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84906-120">CommonParameters</span></span>
<span data-ttu-id="84906-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84906-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84906-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84906-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84906-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84906-123">INPUTS</span></span>

### <span data-ttu-id="84906-124">System. String</span><span class="sxs-lookup"><span data-stu-id="84906-124">System.String</span></span>

### <span data-ttu-id="84906-125">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="84906-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="84906-126">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="84906-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="84906-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84906-127">OUTPUTS</span></span>

### <span data-ttu-id="84906-128">System. String</span><span class="sxs-lookup"><span data-stu-id="84906-128">System.String</span></span>

## <span data-ttu-id="84906-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84906-129">NOTES</span></span>

## <span data-ttu-id="84906-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84906-130">RELATED LINKS</span></span>

[<span data-ttu-id="84906-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="84906-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


