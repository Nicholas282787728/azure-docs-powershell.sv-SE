---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923613"
---
# <span data-ttu-id="e0b67-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e0b67-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="e0b67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0b67-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b67-103">Hämtar lagrings resursanvändningen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e0b67-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="e0b67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0b67-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0b67-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0b67-105">DESCRIPTION</span></span>
<span data-ttu-id="e0b67-106">Cmdleten **Get-AzStorageUsage** hämtar resursanvändningen för Azure Storage för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e0b67-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="e0b67-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0b67-107">EXAMPLES</span></span>

### <span data-ttu-id="e0b67-108">Exempel 1: skaffa användning av lagrings resurser</span><span class="sxs-lookup"><span data-stu-id="e0b67-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="e0b67-109">Det här kommandot får användning av lagrings resurserna för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="e0b67-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="e0b67-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0b67-110">PARAMETERS</span></span>

### <span data-ttu-id="e0b67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b67-111">-DefaultProfile</span></span>
<span data-ttu-id="e0b67-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0b67-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0b67-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b67-113">CommonParameters</span></span>
<span data-ttu-id="e0b67-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0b67-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b67-115">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0b67-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b67-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0b67-116">INPUTS</span></span>

### <span data-ttu-id="e0b67-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="e0b67-117">None</span></span>

## <span data-ttu-id="e0b67-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0b67-118">OUTPUTS</span></span>

### <span data-ttu-id="e0b67-119">Microsoft. Azure. commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="e0b67-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="e0b67-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0b67-120">NOTES</span></span>

## <span data-ttu-id="e0b67-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0b67-121">RELATED LINKS</span></span>

[<span data-ttu-id="e0b67-122">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="e0b67-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


