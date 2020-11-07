---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 3505a2b18ac35644fe401dea4aca8c96b10a7f2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744021"
---
# <span data-ttu-id="02107-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="02107-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="02107-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02107-102">SYNOPSIS</span></span>
<span data-ttu-id="02107-103">Skapar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="02107-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="02107-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02107-104">SYNTAX</span></span>

### <span data-ttu-id="02107-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="02107-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02107-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="02107-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02107-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02107-107">DESCRIPTION</span></span>
<span data-ttu-id="02107-108">Skapar en för angiven IotHub.</span><span class="sxs-lookup"><span data-stu-id="02107-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="02107-109">De här namnen är inte unika och måste hanteras noggrant.</span><span class="sxs-lookup"><span data-stu-id="02107-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="02107-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02107-110">EXAMPLES</span></span>

### <span data-ttu-id="02107-111">Exempel 1 lägga till en IotHub</span><span class="sxs-lookup"><span data-stu-id="02107-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="02107-112">Skapar en Key med namnet "MyKey" för iothub "myiothub" med RegistryRead-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="02107-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="02107-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02107-113">PARAMETERS</span></span>

### <span data-ttu-id="02107-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02107-114">-DefaultProfile</span></span>
<span data-ttu-id="02107-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="02107-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02107-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="02107-116">-HubId</span></span>
<span data-ttu-id="02107-117">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="02107-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="02107-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="02107-118">-KeyName</span></span>
<span data-ttu-id="02107-119">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="02107-119">Name of the Key</span></span>

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

### <span data-ttu-id="02107-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="02107-120">-Name</span></span>
<span data-ttu-id="02107-121">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="02107-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="02107-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="02107-122">-PrimaryKey</span></span>
<span data-ttu-id="02107-123">Primärt</span><span class="sxs-lookup"><span data-stu-id="02107-123">The primary key</span></span>

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

### <span data-ttu-id="02107-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02107-124">-ResourceGroupName</span></span>
<span data-ttu-id="02107-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="02107-125">Resource Group Name</span></span>

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

### <span data-ttu-id="02107-126">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="02107-126">-Rights</span></span>
<span data-ttu-id="02107-127">Behörigheterna för den här IOTHub</span><span class="sxs-lookup"><span data-stu-id="02107-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02107-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="02107-128">-SecondaryKey</span></span>
<span data-ttu-id="02107-129">Sekundärt-tangenten</span><span class="sxs-lookup"><span data-stu-id="02107-129">The Secondary Key</span></span>

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

### <span data-ttu-id="02107-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02107-130">-Confirm</span></span>
<span data-ttu-id="02107-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02107-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02107-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02107-132">-WhatIf</span></span>
<span data-ttu-id="02107-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02107-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02107-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02107-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02107-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02107-135">CommonParameters</span></span>
<span data-ttu-id="02107-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02107-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02107-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02107-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02107-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02107-138">INPUTS</span></span>

### <span data-ttu-id="02107-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02107-139">System.String</span></span>

## <span data-ttu-id="02107-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02107-140">OUTPUTS</span></span>

### <span data-ttu-id="02107-141">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="02107-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="02107-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02107-142">NOTES</span></span>

## <span data-ttu-id="02107-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02107-143">RELATED LINKS</span></span>