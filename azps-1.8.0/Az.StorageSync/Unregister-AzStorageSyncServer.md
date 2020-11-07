---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746194"
---
# <span data-ttu-id="2139a-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="2139a-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="2139a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2139a-102">SYNOPSIS</span></span>
<span data-ttu-id="2139a-103">Varning! om du avregistrerar en server kommer alla Server slut punkter att tas bort från den här servern.</span><span class="sxs-lookup"><span data-stu-id="2139a-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="2139a-104">Det här kommandot avregistrerar en server och tjänsten Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="2139a-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="2139a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2139a-105">SYNTAX</span></span>

### <span data-ttu-id="2139a-106">InputObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2139a-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2139a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2139a-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2139a-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2139a-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2139a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2139a-109">DESCRIPTION</span></span>
<span data-ttu-id="2139a-110">Det här kommandot avregistrerar en server från Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2139a-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="2139a-111">Varning! om du avregistrerar en server kommer alla Server slut punkter att tas bort från den här servern.</span><span class="sxs-lookup"><span data-stu-id="2139a-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="2139a-112">Den bör bara anropas om du är säker på att det inte finns någon sökväg på den här servern längre.</span><span class="sxs-lookup"><span data-stu-id="2139a-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="2139a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2139a-113">EXAMPLES</span></span>

### <span data-ttu-id="2139a-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2139a-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="2139a-115">Det här kommandot avregistrerar servern och skapar borttagning av alla Server slut punkter på servern.</span><span class="sxs-lookup"><span data-stu-id="2139a-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="2139a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2139a-116">PARAMETERS</span></span>

### <span data-ttu-id="2139a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2139a-117">-AsJob</span></span>
<span data-ttu-id="2139a-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2139a-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2139a-119">-DefaultProfile</span></span>
<span data-ttu-id="2139a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2139a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2139a-121">-Force</span></span>
<span data-ttu-id="2139a-122">Försörjning-Force för att hoppa över bekräftelsen av det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="2139a-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2139a-123">-InputObject</span></span>
<span data-ttu-id="2139a-124">RegisteredServer-textobjekt, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="2139a-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2139a-125">-PassThru</span></span>
<span data-ttu-id="2139a-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="2139a-126">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2139a-127">-ResourceGroupName</span></span>
<span data-ttu-id="2139a-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2139a-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2139a-129">-ResourceId</span></span>
<span data-ttu-id="2139a-130">RegisteredServer-resurs-ID</span><span class="sxs-lookup"><span data-stu-id="2139a-130">RegisteredServer Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-131">-ServerId</span><span class="sxs-lookup"><span data-stu-id="2139a-131">-ServerId</span></span>
<span data-ttu-id="2139a-132">Namn på RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="2139a-132">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2139a-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="2139a-134">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2139a-134">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2139a-135">-Confirm</span></span>
<span data-ttu-id="2139a-136">Här visas en uppmaning om att bekräfta innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2139a-136">Prompts for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2139a-137">-WhatIf</span></span>
<span data-ttu-id="2139a-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2139a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2139a-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2139a-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2139a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2139a-140">CommonParameters</span></span>
<span data-ttu-id="2139a-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2139a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2139a-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2139a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2139a-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2139a-143">INPUTS</span></span>

### <span data-ttu-id="2139a-144">Microsoft. Azure. commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="2139a-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="2139a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2139a-145">System.String</span></span>

### <span data-ttu-id="2139a-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2139a-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2139a-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2139a-147">OUTPUTS</span></span>

### <span data-ttu-id="2139a-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="2139a-148">System.Object</span></span>
## <span data-ttu-id="2139a-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2139a-149">NOTES</span></span>

## <span data-ttu-id="2139a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2139a-150">RELATED LINKS</span></span>
