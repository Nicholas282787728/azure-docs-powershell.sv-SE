---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103449"
---
# <span data-ttu-id="95056-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="95056-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="95056-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95056-102">SYNOPSIS</span></span>
<span data-ttu-id="95056-103">Skapar en ny roll för en enhet</span><span class="sxs-lookup"><span data-stu-id="95056-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="95056-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95056-104">SYNTAX</span></span>

### <span data-ttu-id="95056-105">ConnectionStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="95056-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95056-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="95056-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95056-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95056-107">DESCRIPTION</span></span>
<span data-ttu-id="95056-108">Cmdleten **New-AzStackEdgeRole** skapar en ny roll för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="95056-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="95056-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95056-109">EXAMPLES</span></span>

### <span data-ttu-id="95056-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="95056-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="95056-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95056-111">PARAMETERS</span></span>

### <span data-ttu-id="95056-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95056-112">-AsJob</span></span>
<span data-ttu-id="95056-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="95056-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95056-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="95056-114">-ConnectionString</span></span>
<span data-ttu-id="95056-115">Så här anger du anslutnings strängar</span><span class="sxs-lookup"><span data-stu-id="95056-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="95056-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95056-116">-DefaultProfile</span></span>
<span data-ttu-id="95056-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95056-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95056-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="95056-118">-DeviceName</span></span>
<span data-ttu-id="95056-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="95056-119">Device Name</span></span>

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

### <span data-ttu-id="95056-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="95056-120">-DeviceProperty</span></span>
<span data-ttu-id="95056-121">Så här tillhandahåller du enhets egenskaper</span><span class="sxs-lookup"><span data-stu-id="95056-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="95056-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="95056-122">-EncryptionKey</span></span>
<span data-ttu-id="95056-123">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="95056-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="95056-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="95056-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="95056-125">Åtkomst nycklar för IoT-enhet</span><span class="sxs-lookup"><span data-stu-id="95056-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="95056-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="95056-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="95056-127">Ange anslutnings sträng för IOT-enhet</span><span class="sxs-lookup"><span data-stu-id="95056-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="95056-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="95056-128">-IotDeviceId</span></span>
<span data-ttu-id="95056-129">Enhets-ID för IoT-enheten</span><span class="sxs-lookup"><span data-stu-id="95056-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="95056-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="95056-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="95056-131">Snabb tangenten för IoT Edge-enheten</span><span class="sxs-lookup"><span data-stu-id="95056-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="95056-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="95056-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="95056-133">Ange anslutnings sträng för Edge-enhet</span><span class="sxs-lookup"><span data-stu-id="95056-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="95056-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="95056-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="95056-135">ID för IoT Edge-enheten</span><span class="sxs-lookup"><span data-stu-id="95056-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="95056-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="95056-136">-IotHostHub</span></span>
<span data-ttu-id="95056-137">Hosthub-adress</span><span class="sxs-lookup"><span data-stu-id="95056-137">Hosthub address</span></span>

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

### <span data-ttu-id="95056-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="95056-138">-Name</span></span>
<span data-ttu-id="95056-139">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="95056-139">Resource Name</span></span>

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

### <span data-ttu-id="95056-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="95056-140">-Platform</span></span>
<span data-ttu-id="95056-141">Ange plattformen för: Linux</span><span class="sxs-lookup"><span data-stu-id="95056-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="95056-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95056-142">-ResourceGroupName</span></span>
<span data-ttu-id="95056-143">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="95056-143">Resource Group Name</span></span>

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

### <span data-ttu-id="95056-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="95056-144">-RoleStatus</span></span>
<span data-ttu-id="95056-145">Ange status aktivera/inaktivera</span><span class="sxs-lookup"><span data-stu-id="95056-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="95056-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95056-146">-Confirm</span></span>
<span data-ttu-id="95056-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95056-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95056-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95056-148">-WhatIf</span></span>
<span data-ttu-id="95056-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95056-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95056-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95056-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95056-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95056-151">CommonParameters</span></span>
<span data-ttu-id="95056-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95056-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95056-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95056-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95056-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95056-154">INPUTS</span></span>

### <span data-ttu-id="95056-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="95056-155">None</span></span>

## <span data-ttu-id="95056-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95056-156">OUTPUTS</span></span>

### <span data-ttu-id="95056-157">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="95056-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="95056-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95056-158">NOTES</span></span>

## <span data-ttu-id="95056-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95056-159">RELATED LINKS</span></span>
