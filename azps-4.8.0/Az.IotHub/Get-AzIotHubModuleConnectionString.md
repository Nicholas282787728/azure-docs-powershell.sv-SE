---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262646"
---
# <span data-ttu-id="27326-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="27326-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="27326-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27326-102">SYNOPSIS</span></span>
<span data-ttu-id="27326-103">Skaffa anslutnings strängen för en modul för mål-IoT i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27326-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="27326-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27326-104">SYNTAX</span></span>

### <span data-ttu-id="27326-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="27326-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27326-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="27326-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27326-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="27326-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27326-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27326-108">DESCRIPTION</span></span>
<span data-ttu-id="27326-109">Lista anslutnings sträng för alla moduler eller en angiven modul för en mål-IoT-enhet i ett Azure IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27326-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="27326-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27326-110">EXAMPLES</span></span>

### <span data-ttu-id="27326-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27326-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="27326-112">Visa alla moduler anslutnings strängar för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27326-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="27326-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="27326-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="27326-114">Hämta den sekundära modulens anslutnings sträng för en mål-IoT-enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="27326-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="27326-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27326-115">PARAMETERS</span></span>

### <span data-ttu-id="27326-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27326-116">-DefaultProfile</span></span>
<span data-ttu-id="27326-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27326-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27326-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="27326-118">-DeviceId</span></span>
<span data-ttu-id="27326-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="27326-119">Target Device Id.</span></span>

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

### <span data-ttu-id="27326-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27326-120">-InputObject</span></span>
<span data-ttu-id="27326-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="27326-121">IotHub object</span></span>

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

### <span data-ttu-id="27326-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="27326-122">-IotHubName</span></span>
<span data-ttu-id="27326-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="27326-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="27326-124">-Värdetyp</span><span class="sxs-lookup"><span data-stu-id="27326-124">-KeyType</span></span>
<span data-ttu-id="27326-125">Typ av policy för delad åtkomst för autentisering.</span><span class="sxs-lookup"><span data-stu-id="27326-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="27326-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="27326-126">-ModuleId</span></span>
<span data-ttu-id="27326-127">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="27326-127">Target Module Id.</span></span>

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

### <span data-ttu-id="27326-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27326-128">-ResourceGroupName</span></span>
<span data-ttu-id="27326-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="27326-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="27326-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27326-130">-ResourceId</span></span>
<span data-ttu-id="27326-131">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="27326-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="27326-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27326-132">CommonParameters</span></span>
<span data-ttu-id="27326-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27326-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27326-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27326-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27326-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27326-135">INPUTS</span></span>

### <span data-ttu-id="27326-136">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="27326-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="27326-137">System. String</span><span class="sxs-lookup"><span data-stu-id="27326-137">System.String</span></span>

## <span data-ttu-id="27326-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27326-138">OUTPUTS</span></span>

### <span data-ttu-id="27326-139">Microsoft. Azure. commands. Management. IotHub. Models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="27326-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="27326-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27326-140">NOTES</span></span>

## <span data-ttu-id="27326-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27326-141">RELATED LINKS</span></span>