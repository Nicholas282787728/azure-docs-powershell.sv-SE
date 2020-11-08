---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260278"
---
# <span data-ttu-id="860d5-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="860d5-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="860d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="860d5-102">SYNOPSIS</span></span>
<span data-ttu-id="860d5-103">Skapar en ny roll för en enhet</span><span class="sxs-lookup"><span data-stu-id="860d5-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="860d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="860d5-104">SYNTAX</span></span>

### <span data-ttu-id="860d5-105">ConnectionStringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="860d5-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="860d5-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="860d5-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="860d5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="860d5-107">DESCRIPTION</span></span>
<span data-ttu-id="860d5-108">Cmdleten **New-AzDataBoxEdgeRole** skapar en ny roll för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="860d5-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="860d5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="860d5-109">EXAMPLES</span></span>

### <span data-ttu-id="860d5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="860d5-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="860d5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="860d5-111">PARAMETERS</span></span>

### <span data-ttu-id="860d5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="860d5-112">-AsJob</span></span>
<span data-ttu-id="860d5-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="860d5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="860d5-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="860d5-114">-ConnectionString</span></span>
<span data-ttu-id="860d5-115">Så här anger du anslutnings strängar</span><span class="sxs-lookup"><span data-stu-id="860d5-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="860d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860d5-116">-DefaultProfile</span></span>
<span data-ttu-id="860d5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="860d5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="860d5-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="860d5-118">-DeviceName</span></span>
<span data-ttu-id="860d5-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="860d5-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860d5-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="860d5-120">-DeviceProperty</span></span>
<span data-ttu-id="860d5-121">Så här tillhandahåller du enhets egenskaper</span><span class="sxs-lookup"><span data-stu-id="860d5-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="860d5-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="860d5-122">-EncryptionKey</span></span>
<span data-ttu-id="860d5-123">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="860d5-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="860d5-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="860d5-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="860d5-125">Åtkomst nycklar för IoT-enhet</span><span class="sxs-lookup"><span data-stu-id="860d5-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="860d5-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="860d5-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="860d5-127">Ange anslutnings sträng för IOT-enhet</span><span class="sxs-lookup"><span data-stu-id="860d5-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="860d5-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="860d5-128">-IotDeviceId</span></span>
<span data-ttu-id="860d5-129">Enhets-ID för IoT-enheten</span><span class="sxs-lookup"><span data-stu-id="860d5-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="860d5-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="860d5-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="860d5-131">Snabb tangenten för IoT Edge-enheten</span><span class="sxs-lookup"><span data-stu-id="860d5-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="860d5-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="860d5-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="860d5-133">Ange anslutnings sträng för Edge-enhet</span><span class="sxs-lookup"><span data-stu-id="860d5-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="860d5-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="860d5-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="860d5-135">ID för IoT Edge-enheten</span><span class="sxs-lookup"><span data-stu-id="860d5-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="860d5-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="860d5-136">-IotHostHub</span></span>
<span data-ttu-id="860d5-137">Hosthub-adress</span><span class="sxs-lookup"><span data-stu-id="860d5-137">Hosthub address</span></span>

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

### <span data-ttu-id="860d5-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="860d5-138">-Name</span></span>
<span data-ttu-id="860d5-139">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="860d5-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860d5-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="860d5-140">-Platform</span></span>
<span data-ttu-id="860d5-141">Ange plattformen för: Linux</span><span class="sxs-lookup"><span data-stu-id="860d5-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="860d5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860d5-142">-ResourceGroupName</span></span>
<span data-ttu-id="860d5-143">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="860d5-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="860d5-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="860d5-144">-RoleStatus</span></span>
<span data-ttu-id="860d5-145">Ange status aktivera/inaktivera</span><span class="sxs-lookup"><span data-stu-id="860d5-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="860d5-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="860d5-146">-Confirm</span></span>
<span data-ttu-id="860d5-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="860d5-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="860d5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="860d5-148">-WhatIf</span></span>
<span data-ttu-id="860d5-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="860d5-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="860d5-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="860d5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="860d5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860d5-151">CommonParameters</span></span>
<span data-ttu-id="860d5-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860d5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860d5-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="860d5-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860d5-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="860d5-154">INPUTS</span></span>

### <span data-ttu-id="860d5-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="860d5-155">None</span></span>

## <span data-ttu-id="860d5-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="860d5-156">OUTPUTS</span></span>

### <span data-ttu-id="860d5-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="860d5-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="860d5-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="860d5-158">NOTES</span></span>

## <span data-ttu-id="860d5-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="860d5-159">RELATED LINKS</span></span>
