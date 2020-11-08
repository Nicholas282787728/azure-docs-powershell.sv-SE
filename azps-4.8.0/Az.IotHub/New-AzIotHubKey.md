---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101477"
---
# <span data-ttu-id="d3309-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d3309-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="d3309-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3309-102">SYNOPSIS</span></span>
<span data-ttu-id="d3309-103">Skapa en Azure IoT Hub-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="d3309-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="d3309-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3309-104">SYNTAX</span></span>

### <span data-ttu-id="d3309-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d3309-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3309-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d3309-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3309-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3309-107">DESCRIPTION</span></span>
<span data-ttu-id="d3309-108">Skapa en Azure IoT Hub-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="d3309-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="d3309-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3309-109">EXAMPLES</span></span>

### <span data-ttu-id="d3309-110">Exempel 1 återskapa primär nyckeln</span><span class="sxs-lookup"><span data-stu-id="d3309-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="d3309-111">Den omgenererade primär nyckeln för auktoriseringsprincipen "testKey" i ett Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="d3309-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="d3309-112">Exempel 2 byter nycklar</span><span class="sxs-lookup"><span data-stu-id="d3309-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="d3309-113">Utbytes nycklar för auktoriseringsprincipen "testKey" i ett Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="d3309-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="d3309-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3309-114">PARAMETERS</span></span>

### <span data-ttu-id="d3309-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3309-115">-DefaultProfile</span></span>
<span data-ttu-id="d3309-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d3309-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3309-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="d3309-117">-HubId</span></span>
<span data-ttu-id="d3309-118">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="d3309-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d3309-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3309-119">-KeyName</span></span>
<span data-ttu-id="d3309-120">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="d3309-120">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3309-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3309-121">-Name</span></span>
<span data-ttu-id="d3309-122">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="d3309-122">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3309-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="d3309-123">-RenewKey</span></span>
<span data-ttu-id="d3309-124">Återskapa nyckeln.</span><span class="sxs-lookup"><span data-stu-id="d3309-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="d3309-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3309-125">-ResourceGroupName</span></span>
<span data-ttu-id="d3309-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d3309-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3309-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3309-127">-Confirm</span></span>
<span data-ttu-id="d3309-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3309-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3309-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3309-129">-WhatIf</span></span>
<span data-ttu-id="d3309-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3309-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3309-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3309-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3309-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3309-132">CommonParameters</span></span>
<span data-ttu-id="d3309-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3309-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3309-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3309-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3309-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3309-135">INPUTS</span></span>

### <span data-ttu-id="d3309-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d3309-136">System.String</span></span>

## <span data-ttu-id="d3309-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3309-137">OUTPUTS</span></span>

### <span data-ttu-id="d3309-138">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d3309-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="d3309-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3309-139">NOTES</span></span>

## <span data-ttu-id="d3309-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3309-140">RELATED LINKS</span></span>
