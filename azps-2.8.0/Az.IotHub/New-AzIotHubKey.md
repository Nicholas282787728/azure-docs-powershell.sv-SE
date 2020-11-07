---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 8e75965b4f69315b6ab94fa7c77e3859e11a4f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743975"
---
# <span data-ttu-id="5f8e1-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="5f8e1-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="5f8e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8e1-103">Skapa en Azure IoT Hub-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="5f8e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f8e1-104">SYNTAX</span></span>

### <span data-ttu-id="5f8e1-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5f8e1-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f8e1-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5f8e1-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f8e1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f8e1-107">DESCRIPTION</span></span>
<span data-ttu-id="5f8e1-108">Skapa en Azure IoT Hub-nyckeln.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="5f8e1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f8e1-109">EXAMPLES</span></span>

### <span data-ttu-id="5f8e1-110">Exempel 1 återskapa primär nyckeln</span><span class="sxs-lookup"><span data-stu-id="5f8e1-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="5f8e1-111">Den omgenererade primär nyckeln för auktoriseringsprincipen "testKey" i ett Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="5f8e1-112">Exempel 2 byter nycklar</span><span class="sxs-lookup"><span data-stu-id="5f8e1-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="5f8e1-113">Utbytes nycklar för auktoriseringsprincipen "testKey" i ett Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="5f8e1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f8e1-114">PARAMETERS</span></span>

### <span data-ttu-id="5f8e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8e1-115">-DefaultProfile</span></span>
<span data-ttu-id="5f8e1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5f8e1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f8e1-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="5f8e1-117">-HubId</span></span>
<span data-ttu-id="5f8e1-118">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="5f8e1-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5f8e1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f8e1-119">-KeyName</span></span>
<span data-ttu-id="5f8e1-120">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="5f8e1-120">Name of the Key</span></span>

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

### <span data-ttu-id="5f8e1-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f8e1-121">-Name</span></span>
<span data-ttu-id="5f8e1-122">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="5f8e1-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="5f8e1-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="5f8e1-123">-RenewKey</span></span>
<span data-ttu-id="5f8e1-124">Återskapa nyckeln.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="5f8e1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8e1-125">-ResourceGroupName</span></span>
<span data-ttu-id="5f8e1-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5f8e1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5f8e1-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f8e1-127">-Confirm</span></span>
<span data-ttu-id="5f8e1-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f8e1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f8e1-129">-WhatIf</span></span>
<span data-ttu-id="5f8e1-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f8e1-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f8e1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8e1-132">CommonParameters</span></span>
<span data-ttu-id="5f8e1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8e1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8e1-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8e1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8e1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f8e1-135">INPUTS</span></span>

### <span data-ttu-id="5f8e1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5f8e1-136">System.String</span></span>

## <span data-ttu-id="5f8e1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f8e1-137">OUTPUTS</span></span>

### <span data-ttu-id="5f8e1-138">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f8e1-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="5f8e1-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f8e1-139">NOTES</span></span>

## <span data-ttu-id="5f8e1-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f8e1-140">RELATED LINKS</span></span>