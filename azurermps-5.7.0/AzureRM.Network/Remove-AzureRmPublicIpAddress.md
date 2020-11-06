---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpAddress.md
ms.openlocfilehash: 60c6a106acec84b3f43a3bd825e7be9b87fe8e70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583643"
---
# <span data-ttu-id="20d8f-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20d8f-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="20d8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="20d8f-103">Tar bort en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="20d8f-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20d8f-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d8f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20d8f-105">DESCRIPTION</span></span>
<span data-ttu-id="20d8f-106">Cmdleten **Remove-AzureRmPublicIpAddress** tar bort en offentlig Azure-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="20d8f-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="20d8f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20d8f-107">EXAMPLES</span></span>

### <span data-ttu-id="20d8f-108">1: ta bort en offentlig IP-adressresurs</span><span class="sxs-lookup"><span data-stu-id="20d8f-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="20d8f-109">Det här kommandot tar bort den offentliga IP-adressresursen som heter $publicIpName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="20d8f-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="20d8f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20d8f-110">PARAMETERS</span></span>

### <span data-ttu-id="20d8f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20d8f-111">-AsJob</span></span>
<span data-ttu-id="20d8f-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="20d8f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20d8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d8f-113">-DefaultProfile</span></span>
<span data-ttu-id="20d8f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20d8f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d8f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="20d8f-115">-Force</span></span>
<span data-ttu-id="20d8f-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="20d8f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20d8f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="20d8f-117">-Name</span></span>
<span data-ttu-id="20d8f-118">Anger namnet på den offentliga IP-adressen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="20d8f-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d8f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20d8f-119">-PassThru</span></span>
<span data-ttu-id="20d8f-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="20d8f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20d8f-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="20d8f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20d8f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d8f-122">-ResourceGroupName</span></span>
<span data-ttu-id="20d8f-123">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="20d8f-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d8f-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20d8f-124">-Confirm</span></span>
<span data-ttu-id="20d8f-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20d8f-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d8f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d8f-126">-WhatIf</span></span>
<span data-ttu-id="20d8f-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20d8f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d8f-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20d8f-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20d8f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d8f-129">CommonParameters</span></span>
<span data-ttu-id="20d8f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d8f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d8f-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d8f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d8f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20d8f-132">INPUTS</span></span>

### <span data-ttu-id="20d8f-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="20d8f-133">None</span></span>
<span data-ttu-id="20d8f-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="20d8f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20d8f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20d8f-135">OUTPUTS</span></span>

## <span data-ttu-id="20d8f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20d8f-136">NOTES</span></span>

## <span data-ttu-id="20d8f-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20d8f-137">RELATED LINKS</span></span>

[<span data-ttu-id="20d8f-138">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20d8f-138">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="20d8f-139">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20d8f-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="20d8f-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="20d8f-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


