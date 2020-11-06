---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582415"
---
# <span data-ttu-id="a5208-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="a5208-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="a5208-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5208-102">SYNOPSIS</span></span>
<span data-ttu-id="a5208-103">Skapar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="a5208-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5208-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5208-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5208-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5208-105">DESCRIPTION</span></span>
<span data-ttu-id="a5208-106">Skapar en för angiven IotHub.</span><span class="sxs-lookup"><span data-stu-id="a5208-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="a5208-107">De här namnen är inte unika och måste hanteras noggrant.</span><span class="sxs-lookup"><span data-stu-id="a5208-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="a5208-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5208-108">EXAMPLES</span></span>

### <span data-ttu-id="a5208-109">Exempel 1 lägga till en IotHub</span><span class="sxs-lookup"><span data-stu-id="a5208-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="a5208-110">Skapar en Key med namnet "MyKey" för iothub "myiothub" med RegistryRead-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="a5208-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="a5208-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5208-111">PARAMETERS</span></span>

### <span data-ttu-id="a5208-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5208-112">-KeyName</span></span>
<span data-ttu-id="a5208-113">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="a5208-113">Name of the Key</span></span>

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

### <span data-ttu-id="a5208-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5208-114">-Name</span></span>
<span data-ttu-id="a5208-115">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="a5208-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="a5208-116">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a5208-116">-PrimaryKey</span></span>
<span data-ttu-id="a5208-117">Primärt</span><span class="sxs-lookup"><span data-stu-id="a5208-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5208-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5208-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5208-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a5208-119">Resource Group Name</span></span>

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

### <span data-ttu-id="a5208-120">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="a5208-120">-Rights</span></span>
<span data-ttu-id="a5208-121">Behörigheterna för den här IOTHub</span><span class="sxs-lookup"><span data-stu-id="a5208-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5208-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a5208-122">-SecondaryKey</span></span>
<span data-ttu-id="a5208-123">Sekundärt-tangenten</span><span class="sxs-lookup"><span data-stu-id="a5208-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5208-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5208-124">-Confirm</span></span>
<span data-ttu-id="a5208-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5208-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5208-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5208-126">-WhatIf</span></span>
<span data-ttu-id="a5208-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5208-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5208-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5208-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5208-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5208-129">-DefaultProfile</span></span>
<span data-ttu-id="a5208-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5208-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5208-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5208-131">CommonParameters</span></span>
<span data-ttu-id="a5208-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5208-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5208-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5208-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5208-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5208-134">INPUTS</span></span>

### <span data-ttu-id="a5208-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a5208-135">System.String</span></span>
<span data-ttu-id="a5208-136">Microsoft. Azure. commands. Management. IotHub. Models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="a5208-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="a5208-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5208-137">OUTPUTS</span></span>

### <span data-ttu-id="a5208-138">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5208-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="a5208-139">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. kommandon. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="a5208-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="a5208-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5208-140">NOTES</span></span>

## <span data-ttu-id="a5208-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5208-141">RELATED LINKS</span></span>

