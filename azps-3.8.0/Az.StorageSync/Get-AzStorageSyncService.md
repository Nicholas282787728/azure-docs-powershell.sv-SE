---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926366"
---
# <span data-ttu-id="bbd31-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bbd31-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="bbd31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbd31-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd31-103">Det här kommandot visar alla lagrings Sync-tjänster i ett givet omfång av abonnemang/resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bbd31-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="bbd31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbd31-104">SYNTAX</span></span>

### <span data-ttu-id="bbd31-105">ParentStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bbd31-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbd31-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbd31-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbd31-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbd31-107">DESCRIPTION</span></span>
<span data-ttu-id="bbd31-108">Det här kommandot visar alla lagrings Sync-tjänster i ett givet omfång av abonnemang/resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bbd31-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="bbd31-109">Den kan också användas för att lista attributen för varje lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="bbd31-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="bbd31-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbd31-110">EXAMPLES</span></span>

### <span data-ttu-id="bbd31-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bbd31-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="bbd31-112">Det här kommandot listar alla resurser för lagrings tjänst i en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bbd31-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="bbd31-113">Den kan också användas för att lista attributen för varje lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="bbd31-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="bbd31-114">Ange-StorageSyncServiceName för att returnera ett specifikt nummer.</span><span class="sxs-lookup"><span data-stu-id="bbd31-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="bbd31-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbd31-115">PARAMETERS</span></span>

### <span data-ttu-id="bbd31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd31-116">-DefaultProfile</span></span>
<span data-ttu-id="bbd31-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bbd31-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd31-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="bbd31-118">-Name</span></span>
<span data-ttu-id="bbd31-119">Namn på Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bbd31-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd31-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd31-120">-ResourceGroupName</span></span>
<span data-ttu-id="bbd31-121">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="bbd31-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbd31-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd31-122">CommonParameters</span></span>
<span data-ttu-id="bbd31-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd31-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd31-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbd31-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd31-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbd31-125">INPUTS</span></span>

### <span data-ttu-id="bbd31-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bbd31-126">System.String</span></span>

## <span data-ttu-id="bbd31-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbd31-127">OUTPUTS</span></span>

### <span data-ttu-id="bbd31-128">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bbd31-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="bbd31-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbd31-129">NOTES</span></span>

## <span data-ttu-id="bbd31-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbd31-130">RELATED LINKS</span></span>