---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 886c8e7227d036e67d3e6f0d2dc04c4e9887e777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575676"
---
# <span data-ttu-id="9df66-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9df66-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="9df66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9df66-102">SYNOPSIS</span></span>
<span data-ttu-id="9df66-103">Hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9df66-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9df66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9df66-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9df66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9df66-105">DESCRIPTION</span></span>
<span data-ttu-id="9df66-106">Cmdleten **Get-AzureRmDataLakeStoreItemOwner** hämtar ägaren till en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9df66-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9df66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9df66-107">EXAMPLES</span></span>

### <span data-ttu-id="9df66-108">Exempel 1: Hämta ägaren till en katalog</span><span class="sxs-lookup"><span data-stu-id="9df66-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="9df66-109">Det här kommandot får användarens ägare till rot katalogen för ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="9df66-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="9df66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9df66-110">PARAMETERS</span></span>

### <span data-ttu-id="9df66-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="9df66-111">-Account</span></span>
<span data-ttu-id="9df66-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="9df66-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9df66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df66-113">-DefaultProfile</span></span>
<span data-ttu-id="9df66-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9df66-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9df66-115">-Path</span><span class="sxs-lookup"><span data-stu-id="9df66-115">-Path</span></span>
<span data-ttu-id="9df66-116">Anger data Lake Store-sökvägen för ett objekt, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="9df66-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9df66-117">– Skriv</span><span class="sxs-lookup"><span data-stu-id="9df66-117">-Type</span></span>
<span data-ttu-id="9df66-118">Anger typen av ägare som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9df66-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="9df66-119">De acceptabla värdena för denna parameter är: User och Group.</span><span class="sxs-lookup"><span data-stu-id="9df66-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9df66-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df66-120">CommonParameters</span></span>
<span data-ttu-id="9df66-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9df66-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df66-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9df66-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df66-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9df66-123">INPUTS</span></span>

### <span data-ttu-id="9df66-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="9df66-124">None</span></span>
<span data-ttu-id="9df66-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9df66-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9df66-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9df66-126">OUTPUTS</span></span>

### <span data-ttu-id="9df66-127">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="9df66-127">string</span></span>
<span data-ttu-id="9df66-128">Ägaren till det angivna objektet.</span><span class="sxs-lookup"><span data-stu-id="9df66-128">The owner of the specified item.</span></span>

## <span data-ttu-id="9df66-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9df66-129">NOTES</span></span>

## <span data-ttu-id="9df66-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9df66-130">RELATED LINKS</span></span>

[<span data-ttu-id="9df66-131">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9df66-131">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


