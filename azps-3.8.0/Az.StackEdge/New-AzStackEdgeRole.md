---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090795"
---
# <span data-ttu-id="4d7f6-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4d7f6-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="4d7f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7f6-103">Skapar en ny roll för en enhet</span><span class="sxs-lookup"><span data-stu-id="4d7f6-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="4d7f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d7f6-104">SYNTAX</span></span>

### <span data-ttu-id="4d7f6-105">ConnectionStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4d7f6-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d7f6-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d7f6-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d7f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d7f6-107">DESCRIPTION</span></span>
<span data-ttu-id="4d7f6-108">Cmdleten **New-AzStackEdgeRole** skapar en ny roll för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="4d7f6-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="4d7f6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d7f6-109">EXAMPLES</span></span>

### <span data-ttu-id="4d7f6-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d7f6-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="4d7f6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d7f6-111">PARAMETERS</span></span>

### <span data-ttu-id="4d7f6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d7f6-112">-AsJob</span></span>
<span data-ttu-id="4d7f6-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4d7f6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d7f6-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="4d7f6-114">-ConnectionString</span></span>
<span data-ttu-id="4d7f6-115">Så här anger du anslutnings strängar</span><span class="sxs-lookup"><span data-stu-id="4d7f6-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7f6-116">-DefaultProfile</span></span>
<span data-ttu-id="4d7f6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d7f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d7f6-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="4d7f6-118">-DeviceName</span></span>
<span data-ttu-id="4d7f6-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="4d7f6-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="4d7f6-120">-DeviceProperty</span></span>
<span data-ttu-id="4d7f6-121">Så här tillhandahåller du enhets egenskaper</span><span class="sxs-lookup"><span data-stu-id="4d7f6-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="4d7f6-122">-EncryptionKey</span></span>
<span data-ttu-id="4d7f6-123">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="4d7f6-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="4d7f6-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="4d7f6-125">Åtkomst nycklar för IoT-enhet</span><span class="sxs-lookup"><span data-stu-id="4d7f6-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4d7f6-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="4d7f6-127">Ange anslutnings sträng för IOT-enhet</span><span class="sxs-lookup"><span data-stu-id="4d7f6-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="4d7f6-128">-IotDeviceId</span></span>
<span data-ttu-id="4d7f6-129">Enhets-ID för IoT-enheten</span><span class="sxs-lookup"><span data-stu-id="4d7f6-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="4d7f6-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="4d7f6-131">Snabb tangenten för IoT Edge-enheten</span><span class="sxs-lookup"><span data-stu-id="4d7f6-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="4d7f6-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="4d7f6-133">Ange anslutnings sträng för Edge-enhet</span><span class="sxs-lookup"><span data-stu-id="4d7f6-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="4d7f6-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="4d7f6-135">ID för IoT Edge-enheten</span><span class="sxs-lookup"><span data-stu-id="4d7f6-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="4d7f6-136">-IotHostHub</span></span>
<span data-ttu-id="4d7f6-137">Hosthub-adress</span><span class="sxs-lookup"><span data-stu-id="4d7f6-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d7f6-138">-Name</span></span>
<span data-ttu-id="4d7f6-139">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="4d7f6-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="4d7f6-140">-Platform</span></span>
<span data-ttu-id="4d7f6-141">Ange plattformen för: Linux</span><span class="sxs-lookup"><span data-stu-id="4d7f6-141">Provide the Platform, for ex: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d7f6-142">-ResourceGroupName</span></span>
<span data-ttu-id="4d7f6-143">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4d7f6-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d7f6-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="4d7f6-144">-RoleStatus</span></span>
<span data-ttu-id="4d7f6-145">Ange status aktivera/inaktivera</span><span class="sxs-lookup"><span data-stu-id="4d7f6-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="4d7f6-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d7f6-146">-Confirm</span></span>
<span data-ttu-id="4d7f6-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d7f6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d7f6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d7f6-148">-WhatIf</span></span>
<span data-ttu-id="4d7f6-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d7f6-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d7f6-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d7f6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d7f6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7f6-151">CommonParameters</span></span>
<span data-ttu-id="4d7f6-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7f6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7f6-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d7f6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7f6-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d7f6-154">INPUTS</span></span>

### <span data-ttu-id="4d7f6-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d7f6-155">None</span></span>

## <span data-ttu-id="4d7f6-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d7f6-156">OUTPUTS</span></span>

### <span data-ttu-id="4d7f6-157">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4d7f6-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="4d7f6-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d7f6-158">NOTES</span></span>

## <span data-ttu-id="4d7f6-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d7f6-159">RELATED LINKS</span></span>