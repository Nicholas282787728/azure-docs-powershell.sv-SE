---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
ms.openlocfilehash: 6b537811f47399d3be6b5d6485a492f7623a84c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577205"
---
# <span data-ttu-id="5f153-101">Get-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="5f153-101">Get-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="5f153-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f153-102">SYNOPSIS</span></span>
<span data-ttu-id="5f153-103">Visar alla certifikat eller ett visst certifikat som ingår i ett Azure IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="5f153-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f153-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f153-104">SYNTAX</span></span>

### <span data-ttu-id="5f153-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5f153-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f153-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5f153-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f153-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5f153-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f153-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f153-108">DESCRIPTION</span></span>
<span data-ttu-id="5f153-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="5f153-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="5f153-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f153-110">EXAMPLES</span></span>

### <span data-ttu-id="5f153-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5f153-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="5f153-112">Lista alla certifikat i MyIotHub</span><span class="sxs-lookup"><span data-stu-id="5f153-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="5f153-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5f153-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="5f153-114">Visa information om ett certifikat</span><span class="sxs-lookup"><span data-stu-id="5f153-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="5f153-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f153-115">PARAMETERS</span></span>

### <span data-ttu-id="5f153-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5f153-116">-CertificateName</span></span>
<span data-ttu-id="5f153-117">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="5f153-117">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f153-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f153-118">-DefaultProfile</span></span>
<span data-ttu-id="5f153-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f153-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f153-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f153-120">-InputObject</span></span>
<span data-ttu-id="5f153-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="5f153-121">IotHub Object</span></span>

```yaml
Type: PSIotHub
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f153-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f153-122">-Name</span></span>
<span data-ttu-id="5f153-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="5f153-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f153-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f153-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f153-125">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="5f153-125">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f153-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f153-126">-ResourceId</span></span>
<span data-ttu-id="5f153-127">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="5f153-127">IotHub Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f153-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f153-128">CommonParameters</span></span>
<span data-ttu-id="5f153-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f153-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f153-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f153-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f153-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f153-131">INPUTS</span></span>

### <span data-ttu-id="5f153-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5f153-132">System.String</span></span>

## <span data-ttu-id="5f153-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f153-133">OUTPUTS</span></span>

### <span data-ttu-id="5f153-134">Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="5f153-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="5f153-135">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. Management. IotHub. Models. PSCertificateDescription, Microsoft. Azure. commands. IotHub, version = 3.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5f153-135">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription, Microsoft.Azure.Commands.IotHub, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5f153-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f153-136">NOTES</span></span>

## <span data-ttu-id="5f153-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f153-137">RELATED LINKS</span></span>
