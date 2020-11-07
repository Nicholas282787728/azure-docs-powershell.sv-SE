---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 00236BC2-61D8-49C2-91BE-923C567153F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: af8a85c698a59a31516c6dee05bb57415a45ff62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929681"
---
# <span data-ttu-id="d0a23-101">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0a23-101">Remove-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="d0a23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0a23-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a23-103">Tar bort en offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d0a23-103">Removes a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0a23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0a23-104">SYNTAX</span></span>

```
Remove-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a23-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0a23-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a23-106">Cmdleten **Remove-AzureRmPublicIpAddress** tar bort en offentlig Azure-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d0a23-106">The **Remove-AzureRmPublicIpAddress** cmdlet removes an Azure public IP address.</span></span>

## <span data-ttu-id="d0a23-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0a23-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a23-108">1: ta bort en offentlig IP-adressresurs</span><span class="sxs-lookup"><span data-stu-id="d0a23-108">1: Remove a public IP address resource</span></span>
```
Remove-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="d0a23-109">Det här kommandot tar bort den offentliga IP-adressresursen som heter $publicIpName i resurs gruppen $rgName.</span><span class="sxs-lookup"><span data-stu-id="d0a23-109">This command removes the public IP address resource named $publicIpName in the resource group $rgName.</span></span>

## <span data-ttu-id="d0a23-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0a23-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a23-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0a23-111">-AsJob</span></span>
<span data-ttu-id="d0a23-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d0a23-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0a23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a23-113">-DefaultProfile</span></span>
<span data-ttu-id="d0a23-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0a23-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0a23-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d0a23-115">-Force</span></span>
<span data-ttu-id="d0a23-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d0a23-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0a23-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0a23-117">-Name</span></span>
<span data-ttu-id="d0a23-118">Anger namnet på den offentliga IP-adressen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="d0a23-118">Specifies the name of the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0a23-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0a23-119">-PassThru</span></span>
<span data-ttu-id="d0a23-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d0a23-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0a23-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d0a23-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0a23-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a23-122">-ResourceGroupName</span></span>
<span data-ttu-id="d0a23-123">Anger namnet på den resurs grupp som innehåller den offentliga IP-adressen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="d0a23-123">Specifies the name of the resource group that contains the public IP address that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0a23-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0a23-124">-Confirm</span></span>
<span data-ttu-id="d0a23-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0a23-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a23-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a23-126">-WhatIf</span></span>
<span data-ttu-id="d0a23-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0a23-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a23-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0a23-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a23-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a23-129">CommonParameters</span></span>
<span data-ttu-id="d0a23-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a23-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a23-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a23-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a23-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0a23-132">INPUTS</span></span>

## <span data-ttu-id="d0a23-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0a23-133">OUTPUTS</span></span>

## <span data-ttu-id="d0a23-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0a23-134">NOTES</span></span>

## <span data-ttu-id="d0a23-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0a23-135">RELATED LINKS</span></span>

[<span data-ttu-id="d0a23-136">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0a23-136">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d0a23-137">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0a23-137">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="d0a23-138">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d0a23-138">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


