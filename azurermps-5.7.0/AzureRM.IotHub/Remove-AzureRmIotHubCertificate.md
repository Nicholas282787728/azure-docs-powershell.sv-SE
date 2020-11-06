---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576505"
---
# <span data-ttu-id="c4656-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="c4656-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="c4656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4656-102">SYNOPSIS</span></span>
<span data-ttu-id="c4656-103">Tar bort ett Azure IoT Hub-certifikat.</span><span class="sxs-lookup"><span data-stu-id="c4656-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4656-104">SYNTAX</span></span>

### <span data-ttu-id="c4656-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c4656-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4656-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c4656-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4656-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c4656-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4656-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4656-108">DESCRIPTION</span></span>
<span data-ttu-id="c4656-109">En detaljerad förklaring av CERTIFIKATUTFÄRDARCERTIFIKAT i Azure IoT Hub finns i https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="c4656-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="c4656-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4656-110">EXAMPLES</span></span>

### <span data-ttu-id="c4656-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4656-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="c4656-112">Tar bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="c4656-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="c4656-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4656-113">PARAMETERS</span></span>

### <span data-ttu-id="c4656-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c4656-114">-CertificateName</span></span>
<span data-ttu-id="c4656-115">Namn på certifikatet</span><span class="sxs-lookup"><span data-stu-id="c4656-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="c4656-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4656-116">-DefaultProfile</span></span>
<span data-ttu-id="c4656-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4656-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4656-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="c4656-118">-Etag</span></span>
<span data-ttu-id="c4656-119">Etag för certifikatet</span><span class="sxs-lookup"><span data-stu-id="c4656-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4656-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4656-120">-InputObject</span></span>
<span data-ttu-id="c4656-121">Certifikat objekt</span><span class="sxs-lookup"><span data-stu-id="c4656-121">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4656-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4656-122">-Name</span></span>
<span data-ttu-id="c4656-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="c4656-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4656-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4656-124">-PassThru</span></span>
<span data-ttu-id="c4656-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c4656-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4656-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4656-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4656-127">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c4656-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c4656-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4656-128">-ResourceId</span></span>
<span data-ttu-id="c4656-129">Resurs-ID för certifikat</span><span class="sxs-lookup"><span data-stu-id="c4656-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="c4656-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4656-130">-Confirm</span></span>
<span data-ttu-id="c4656-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4656-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4656-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4656-132">-WhatIf</span></span>
<span data-ttu-id="c4656-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4656-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4656-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4656-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4656-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4656-135">CommonParameters</span></span>
<span data-ttu-id="c4656-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4656-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4656-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4656-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4656-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4656-138">INPUTS</span></span>

### <span data-ttu-id="c4656-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c4656-139">System.String</span></span>

## <span data-ttu-id="c4656-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4656-140">OUTPUTS</span></span>

### <span data-ttu-id="c4656-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4656-141">System.Boolean</span></span>

## <span data-ttu-id="c4656-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4656-142">NOTES</span></span>

## <span data-ttu-id="c4656-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4656-143">RELATED LINKS</span></span>

