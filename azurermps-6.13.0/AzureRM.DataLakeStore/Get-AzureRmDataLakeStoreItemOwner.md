---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4276b9477e51165e01c716095d5f4e2a4ea6ca69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575225"
---
# <span data-ttu-id="03469-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="03469-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="03469-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03469-102">SYNOPSIS</span></span>
<span data-ttu-id="03469-103">Hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03469-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03469-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03469-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03469-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03469-105">DESCRIPTION</span></span>
<span data-ttu-id="03469-106">Cmdleten **Get-AzureRmDataLakeStoreItemOwner** hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03469-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="03469-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03469-107">EXAMPLES</span></span>

### <span data-ttu-id="03469-108">Exempel 1: Hämta ägaren till en katalog</span><span class="sxs-lookup"><span data-stu-id="03469-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="03469-109">Det här kommandot får användarens ägare till rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="03469-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="03469-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03469-110">PARAMETERS</span></span>

### <span data-ttu-id="03469-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="03469-111">-Account</span></span>
<span data-ttu-id="03469-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="03469-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="03469-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03469-113">-DefaultProfile</span></span>
<span data-ttu-id="03469-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03469-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03469-115">-Path</span><span class="sxs-lookup"><span data-stu-id="03469-115">-Path</span></span>
<span data-ttu-id="03469-116">Anger data Lake Store-sökvägen för ett objekt, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="03469-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="03469-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="03469-117">-Type</span></span>
<span data-ttu-id="03469-118">Anger typen av ägare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="03469-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="03469-119">De acceptabla värdena för denna parameter är: User och Group.</span><span class="sxs-lookup"><span data-stu-id="03469-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="03469-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03469-120">CommonParameters</span></span>
<span data-ttu-id="03469-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03469-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03469-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03469-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03469-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03469-123">INPUTS</span></span>

### <span data-ttu-id="03469-124">System. String</span><span class="sxs-lookup"><span data-stu-id="03469-124">System.String</span></span>

### <span data-ttu-id="03469-125">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="03469-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="03469-126">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="03469-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="03469-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03469-127">OUTPUTS</span></span>

### <span data-ttu-id="03469-128">System. String</span><span class="sxs-lookup"><span data-stu-id="03469-128">System.String</span></span>
<span data-ttu-id="03469-129">Ägaren till det angivna objektet.</span><span class="sxs-lookup"><span data-stu-id="03469-129">The owner of the specified item.</span></span>

## <span data-ttu-id="03469-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03469-130">NOTES</span></span>

## <span data-ttu-id="03469-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03469-131">RELATED LINKS</span></span>

[<span data-ttu-id="03469-132">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="03469-132">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


