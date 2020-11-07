---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746198"
---
# <span data-ttu-id="b7f50-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="b7f50-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="b7f50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7f50-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f50-103">Används endast för fel sökning.</span><span class="sxs-lookup"><span data-stu-id="b7f50-103">Use for troubleshooting only.</span></span> <span data-ttu-id="b7f50-104">Det här kommandot återställer Server certifikatet för lagringstester som används för att beskriva Server identiteten för Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b7f50-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="b7f50-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7f50-105">SYNTAX</span></span>

### <span data-ttu-id="b7f50-106">ObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b7f50-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f50-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f50-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f50-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f50-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f50-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7f50-109">DESCRIPTION</span></span>
<span data-ttu-id="b7f50-110">Det här kommandot återställer Server certifikatet för lagrings utrymme som används för att beskriva Server identiteten för Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b7f50-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="b7f50-111">Detta är avsett att användas i fel söknings scenarier.</span><span class="sxs-lookup"><span data-stu-id="b7f50-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="b7f50-112">När du anropar det här kommandot ersätts Server certifikatet, uppdatering av lagrings tjänsten som den här servern är registrerad tillsammans med, genom att den offentliga delen av nycklarna skickas.</span><span class="sxs-lookup"><span data-stu-id="b7f50-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="b7f50-113">Eftersom ett nytt certifikat skapas, uppdateras också förfallo tiden för detta certifikat.</span><span class="sxs-lookup"><span data-stu-id="b7f50-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="b7f50-114">Det här kommandot kan även användas för att uppdatera ett certifikat som har upphört att gälla.</span><span class="sxs-lookup"><span data-stu-id="b7f50-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="b7f50-115">Det här kan inträffa om en server är offline under en längre tid.</span><span class="sxs-lookup"><span data-stu-id="b7f50-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="b7f50-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7f50-116">EXAMPLES</span></span>

### <span data-ttu-id="b7f50-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7f50-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="b7f50-118">Det här kommandot återställer det lokala Server certifikatet och meddelar motsvarande lagrings synkroniseringstjänst för serverns nya identitet på ett säkert sätt.</span><span class="sxs-lookup"><span data-stu-id="b7f50-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="b7f50-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7f50-119">PARAMETERS</span></span>

### <span data-ttu-id="b7f50-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f50-120">-DefaultProfile</span></span>
<span data-ttu-id="b7f50-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f50-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f50-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b7f50-122">-ParentObject</span></span>
<span data-ttu-id="b7f50-123">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="b7f50-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f50-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b7f50-124">-ParentResourceId</span></span>
<span data-ttu-id="b7f50-125">Överordnat resurs-ID för StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b7f50-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f50-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7f50-126">-PassThru</span></span>
<span data-ttu-id="b7f50-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b7f50-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b7f50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f50-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7f50-129">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b7f50-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7f50-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b7f50-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="b7f50-131">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b7f50-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f50-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7f50-132">-Confirm</span></span>
<span data-ttu-id="b7f50-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7f50-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f50-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f50-134">-WhatIf</span></span>
<span data-ttu-id="b7f50-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7f50-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7f50-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7f50-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f50-137">CommonParameters</span></span>
<span data-ttu-id="b7f50-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f50-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7f50-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f50-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7f50-140">INPUTS</span></span>

### <span data-ttu-id="b7f50-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b7f50-141">System.String</span></span>

### <span data-ttu-id="b7f50-142">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b7f50-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b7f50-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7f50-143">OUTPUTS</span></span>

### <span data-ttu-id="b7f50-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="b7f50-144">System.Object</span></span>
## <span data-ttu-id="b7f50-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7f50-145">NOTES</span></span>

## <span data-ttu-id="b7f50-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7f50-146">RELATED LINKS</span></span>
