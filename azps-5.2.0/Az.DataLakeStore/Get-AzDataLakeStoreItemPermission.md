---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400360"
---
# <span data-ttu-id="9306f-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="9306f-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="9306f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9306f-102">SYNOPSIS</span></span>
<span data-ttu-id="9306f-103">Får behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9306f-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9306f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9306f-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9306f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9306f-105">DESCRIPTION</span></span>
<span data-ttu-id="9306f-106">Cmdleten **Get-AzDataLakeStoreItemPermission** får behörigheten oktalt för en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9306f-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9306f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9306f-107">EXAMPLES</span></span>

### <span data-ttu-id="9306f-108">Exempel 1: Ange behörigheten oktalt för en fil</span><span class="sxs-lookup"><span data-stu-id="9306f-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="9306f-109">Det här kommandot får behörigheten oktalt för en fil.</span><span class="sxs-lookup"><span data-stu-id="9306f-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="9306f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9306f-110">PARAMETERS</span></span>

### <span data-ttu-id="9306f-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="9306f-111">-Account</span></span>
<span data-ttu-id="9306f-112">Anger namnet på data Lake Store-butiken.</span><span class="sxs-lookup"><span data-stu-id="9306f-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="9306f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9306f-113">-DefaultProfile</span></span>
<span data-ttu-id="9306f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9306f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9306f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="9306f-115">-Path</span></span>
<span data-ttu-id="9306f-116">Anger data Lake Store-sökvägen till filen eller mappen, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="9306f-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9306f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9306f-117">CommonParameters</span></span>
<span data-ttu-id="9306f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9306f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9306f-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9306f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9306f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9306f-120">INPUTS</span></span>

### <span data-ttu-id="9306f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9306f-121">System.String</span></span>

### <span data-ttu-id="9306f-122">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9306f-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="9306f-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9306f-123">OUTPUTS</span></span>

### <span data-ttu-id="9306f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9306f-124">System.String</span></span>

## <span data-ttu-id="9306f-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9306f-125">NOTES</span></span>
* <span data-ttu-id="9306f-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="9306f-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="9306f-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9306f-127">RELATED LINKS</span></span>

[<span data-ttu-id="9306f-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="9306f-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


