---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 0f1b6806565a21b106816019c08641e269c4d5a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270837"
---
# <span data-ttu-id="fb301-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="fb301-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="fb301-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb301-102">SYNOPSIS</span></span>
<span data-ttu-id="fb301-103">Hämtar information om en ögonblicks bild av Azure NetApp-filer (ANF).</span><span class="sxs-lookup"><span data-stu-id="fb301-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="fb301-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb301-104">SYNTAX</span></span>

### <span data-ttu-id="fb301-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fb301-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb301-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb301-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb301-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb301-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb301-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb301-108">DESCRIPTION</span></span>
<span data-ttu-id="fb301-109">Cmdleten **Get-AzNetAppFilesSnapshot** hämtar information om en ANF-stillbild.</span><span class="sxs-lookup"><span data-stu-id="fb301-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="fb301-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb301-110">EXAMPLES</span></span>

### <span data-ttu-id="fb301-111">Exempel 1: skaffa en ANF-stillbild</span><span class="sxs-lookup"><span data-stu-id="fb301-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="fb301-112">Det här kommandot får den ögonblicks bild som heter MyAnfSnapshot från volymen "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="fb301-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="fb301-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb301-113">PARAMETERS</span></span>

### <span data-ttu-id="fb301-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb301-114">-AccountName</span></span>
<span data-ttu-id="fb301-115">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="fb301-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb301-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb301-116">-DefaultProfile</span></span>
<span data-ttu-id="fb301-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb301-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb301-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb301-118">-Name</span></span>
<span data-ttu-id="fb301-119">Namn på ANF ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="fb301-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb301-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fb301-120">-PoolName</span></span>
<span data-ttu-id="fb301-121">Namnet på ANF-poolen</span><span class="sxs-lookup"><span data-stu-id="fb301-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb301-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb301-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb301-123">ANF-volymens resurs grupp</span><span class="sxs-lookup"><span data-stu-id="fb301-123">The resource group of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb301-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb301-124">-ResourceId</span></span>
<span data-ttu-id="fb301-125">Resurs-ID för ANF ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="fb301-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb301-126">-Volym namn</span><span class="sxs-lookup"><span data-stu-id="fb301-126">-VolumeName</span></span>
<span data-ttu-id="fb301-127">Namnet på ANF-volymen</span><span class="sxs-lookup"><span data-stu-id="fb301-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb301-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="fb301-128">-VolumeObject</span></span>
<span data-ttu-id="fb301-129">Volume-objektet som innehåller den ögonblicks bild som ska returneras</span><span class="sxs-lookup"><span data-stu-id="fb301-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb301-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb301-130">CommonParameters</span></span>
<span data-ttu-id="fb301-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb301-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb301-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb301-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb301-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb301-133">INPUTS</span></span>

### <span data-ttu-id="fb301-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fb301-134">System.String</span></span>

### <span data-ttu-id="fb301-135">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fb301-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fb301-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb301-136">OUTPUTS</span></span>

### <span data-ttu-id="fb301-137">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="fb301-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="fb301-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb301-138">NOTES</span></span>

## <span data-ttu-id="fb301-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb301-139">RELATED LINKS</span></span>