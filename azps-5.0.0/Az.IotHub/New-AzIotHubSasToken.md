---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270965"
---
# <span data-ttu-id="8eb8a-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="8eb8a-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="8eb8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8eb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb8a-103">Skapa en SAS-token för en måls IoT Hub, enhet eller modul.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="8eb8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8eb8a-104">SYNTAX</span></span>

### <span data-ttu-id="8eb8a-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8eb8a-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8eb8a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8eb8a-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8eb8a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8eb8a-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8eb8a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8eb8a-108">DESCRIPTION</span></span>
<span data-ttu-id="8eb8a-109">För enhetens SAS-token används princip parametern endast för att komma åt enhets registret.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="8eb8a-110">Därför bör policyn ha Läs behörighet till registret.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="8eb8a-111">För IoT Hub-token är principen en del av SAS.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="8eb8a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8eb8a-112">EXAMPLES</span></span>

### <span data-ttu-id="8eb8a-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8eb8a-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="8eb8a-114">Skapa en IoT Hub SAS-token med hjälp av iothubowner-principen och primär nyckeln.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="8eb8a-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8eb8a-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="8eb8a-116">Skapa en IoT Hub SAS-token med registryRead policy och sekundär nyckel.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="8eb8a-117">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8eb8a-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="8eb8a-118">Skapa en enhets-SAS-token med hjälp av iothubowner policy för att få åtkomst till {iothub_name} enhets registret.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="8eb8a-119">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="8eb8a-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="8eb8a-120">Skapa en modul SAS-token med hjälp av iothubowner policy för att få åtkomst till {iothub_name} enhets registret.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="8eb8a-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8eb8a-121">PARAMETERS</span></span>

### <span data-ttu-id="8eb8a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb8a-122">-DefaultProfile</span></span>
<span data-ttu-id="8eb8a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb8a-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8eb8a-124">-DeviceId</span></span>
<span data-ttu-id="8eb8a-125">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-125">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-126">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="8eb8a-126">-Duration</span></span>
<span data-ttu-id="8eb8a-127">Framtida slut för ande (i sekunder) för token som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="8eb8a-128">Standardvärdet är 3600.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eb8a-129">-InputObject</span></span>
<span data-ttu-id="8eb8a-130">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="8eb8a-130">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8eb8a-131">-IotHubName</span></span>
<span data-ttu-id="8eb8a-132">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="8eb8a-132">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="8eb8a-133">-KeyName</span></span>
<span data-ttu-id="8eb8a-134">Namn på snabb tangenten.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-134">Access key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-135">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="8eb8a-135">-KeyType</span></span>
<span data-ttu-id="8eb8a-136">Typ av snabb åtkomst.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="8eb8a-137">-ModuleId</span></span>
<span data-ttu-id="8eb8a-138">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-138">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb8a-139">-ResourceGroupName</span></span>
<span data-ttu-id="8eb8a-140">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="8eb8a-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8eb8a-141">-ResourceId</span></span>
<span data-ttu-id="8eb8a-142">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="8eb8a-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb8a-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8eb8a-143">-Confirm</span></span>
<span data-ttu-id="8eb8a-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eb8a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eb8a-145">-WhatIf</span></span>
<span data-ttu-id="8eb8a-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eb8a-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eb8a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb8a-148">CommonParameters</span></span>
<span data-ttu-id="8eb8a-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb8a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb8a-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb8a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb8a-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8eb8a-151">INPUTS</span></span>

### <span data-ttu-id="8eb8a-152">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8eb8a-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8eb8a-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8eb8a-153">System.String</span></span>

## <span data-ttu-id="8eb8a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8eb8a-154">OUTPUTS</span></span>

### <span data-ttu-id="8eb8a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8eb8a-155">System.String</span></span>

## <span data-ttu-id="8eb8a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8eb8a-156">NOTES</span></span>

## <span data-ttu-id="8eb8a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8eb8a-157">RELATED LINKS</span></span>
