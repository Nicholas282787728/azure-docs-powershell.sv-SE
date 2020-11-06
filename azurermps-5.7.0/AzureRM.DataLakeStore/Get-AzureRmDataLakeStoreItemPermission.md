---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: f76473239661b492c95a356dfb1b381e1093f98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575670"
---
# <span data-ttu-id="1b517-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="1b517-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="1b517-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b517-102">SYNOPSIS</span></span>
<span data-ttu-id="1b517-103">Får behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b517-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b517-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b517-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b517-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b517-105">DESCRIPTION</span></span>
<span data-ttu-id="1b517-106">Cmdleten **Get-AzureRmDataLakeStoreItemPermission** får behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b517-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1b517-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b517-107">EXAMPLES</span></span>

### <span data-ttu-id="1b517-108">Exempel 1: Ange behörigheten oktalt för en fil</span><span class="sxs-lookup"><span data-stu-id="1b517-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="1b517-109">Det här kommandot får behörigheten oktalt för en fil.</span><span class="sxs-lookup"><span data-stu-id="1b517-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="1b517-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b517-110">PARAMETERS</span></span>

### <span data-ttu-id="1b517-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1b517-111">-Account</span></span>
<span data-ttu-id="1b517-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="1b517-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="1b517-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b517-113">-DefaultProfile</span></span>
<span data-ttu-id="1b517-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b517-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b517-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1b517-115">-Path</span></span>
<span data-ttu-id="1b517-116">Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="1b517-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1b517-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b517-117">CommonParameters</span></span>
<span data-ttu-id="1b517-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b517-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b517-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b517-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b517-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b517-120">INPUTS</span></span>

### <span data-ttu-id="1b517-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="1b517-121">None</span></span>
<span data-ttu-id="1b517-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1b517-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b517-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b517-123">OUTPUTS</span></span>

### <span data-ttu-id="1b517-124">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="1b517-124">string</span></span>
<span data-ttu-id="1b517-125">Sträng representationen av ägandet oktala</span><span class="sxs-lookup"><span data-stu-id="1b517-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="1b517-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b517-126">NOTES</span></span>
* <span data-ttu-id="1b517-127">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="1b517-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="1b517-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b517-128">RELATED LINKS</span></span>

[<span data-ttu-id="1b517-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="1b517-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


