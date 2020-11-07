---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: f73cfd1cadff449289bfa82ab1de04d110fb0f1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916506"
---
# <span data-ttu-id="b724d-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b724d-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="b724d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b724d-102">SYNOPSIS</span></span>
<span data-ttu-id="b724d-103">Skapar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="b724d-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="b724d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b724d-104">SYNTAX</span></span>

```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b724d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b724d-105">DESCRIPTION</span></span>
<span data-ttu-id="b724d-106">Skapar en för angiven IotHub.</span><span class="sxs-lookup"><span data-stu-id="b724d-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="b724d-107">De här namnen är inte unika och måste hanteras noggrant.</span><span class="sxs-lookup"><span data-stu-id="b724d-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="b724d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b724d-108">EXAMPLES</span></span>

### <span data-ttu-id="b724d-109">Exempel 1 lägga till en IotHub</span><span class="sxs-lookup"><span data-stu-id="b724d-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="b724d-110">Skapar en Key med namnet "MyKey" för iothub "myiothub" med RegistryRead-behörigheter.</span><span class="sxs-lookup"><span data-stu-id="b724d-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="b724d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b724d-111">PARAMETERS</span></span>

### <span data-ttu-id="b724d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b724d-112">-DefaultProfile</span></span>
<span data-ttu-id="b724d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b724d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b724d-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b724d-114">-KeyName</span></span>
<span data-ttu-id="b724d-115">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="b724d-115">Name of the Key</span></span>

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

### <span data-ttu-id="b724d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b724d-116">-Name</span></span>
<span data-ttu-id="b724d-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="b724d-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="b724d-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b724d-118">-PrimaryKey</span></span>
<span data-ttu-id="b724d-119">Primärt</span><span class="sxs-lookup"><span data-stu-id="b724d-119">The primary key</span></span>

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

### <span data-ttu-id="b724d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b724d-120">-ResourceGroupName</span></span>
<span data-ttu-id="b724d-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b724d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="b724d-122">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="b724d-122">-Rights</span></span>
<span data-ttu-id="b724d-123">Behörigheterna för den här IOTHub</span><span class="sxs-lookup"><span data-stu-id="b724d-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="b724d-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b724d-124">-SecondaryKey</span></span>
<span data-ttu-id="b724d-125">Sekundärt-tangenten</span><span class="sxs-lookup"><span data-stu-id="b724d-125">The Secondary Key</span></span>

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

### <span data-ttu-id="b724d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b724d-126">-Confirm</span></span>
<span data-ttu-id="b724d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b724d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b724d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b724d-128">-WhatIf</span></span>
<span data-ttu-id="b724d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b724d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b724d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b724d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b724d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b724d-131">CommonParameters</span></span>
<span data-ttu-id="b724d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b724d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b724d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b724d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b724d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b724d-134">INPUTS</span></span>

### <span data-ttu-id="b724d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b724d-135">System.String</span></span>

## <span data-ttu-id="b724d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b724d-136">OUTPUTS</span></span>

### <span data-ttu-id="b724d-137">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b724d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b724d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b724d-138">NOTES</span></span>

## <span data-ttu-id="b724d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b724d-139">RELATED LINKS</span></span>
