---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 7d61b7672050cd1efa3868a8a89208c790a684fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920818"
---
# <span data-ttu-id="c647c-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c647c-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="c647c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c647c-102">SYNOPSIS</span></span>
<span data-ttu-id="c647c-103">Hämtar lagrings resursanvändningen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c647c-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="c647c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c647c-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c647c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c647c-105">DESCRIPTION</span></span>
<span data-ttu-id="c647c-106">Cmdleten **Get-AzStorageUsage** hämtar resursanvändningen för Azure Storage för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c647c-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="c647c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c647c-107">EXAMPLES</span></span>

### <span data-ttu-id="c647c-108">Exempel 1: Hämta lagrings resurserna på den angivna platsen</span><span class="sxs-lookup"><span data-stu-id="c647c-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="c647c-109">Det här kommandot hämtar lagrings resurserna för den angivna platsen under den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c647c-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="c647c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c647c-110">PARAMETERS</span></span>

### <span data-ttu-id="c647c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c647c-111">-DefaultProfile</span></span>
<span data-ttu-id="c647c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c647c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c647c-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="c647c-113">-Location</span></span>
<span data-ttu-id="c647c-114">Ange att du vill använda användning av lagrings resurser på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="c647c-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="c647c-115">Om inget anges får du lagrings resurser på alla platser under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c647c-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c647c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c647c-116">CommonParameters</span></span>
<span data-ttu-id="c647c-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c647c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c647c-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c647c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c647c-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c647c-119">INPUTS</span></span>

### <span data-ttu-id="c647c-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c647c-120">System.String</span></span>

## <span data-ttu-id="c647c-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c647c-121">OUTPUTS</span></span>

### <span data-ttu-id="c647c-122">Microsoft. Azure. commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="c647c-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="c647c-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c647c-123">NOTES</span></span>

## <span data-ttu-id="c647c-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c647c-124">RELATED LINKS</span></span>

[<span data-ttu-id="c647c-125">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="c647c-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


