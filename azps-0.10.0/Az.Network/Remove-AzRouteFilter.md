---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 02f3e0a151fe8dc810e8530af88059371139f08c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924354"
---
# <span data-ttu-id="0d111-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0d111-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="0d111-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d111-102">SYNOPSIS</span></span>
<span data-ttu-id="0d111-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="0d111-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="0d111-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d111-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d111-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d111-105">DESCRIPTION</span></span>
<span data-ttu-id="0d111-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="0d111-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0d111-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d111-107">EXAMPLES</span></span>

### <span data-ttu-id="0d111-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d111-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0d111-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="0d111-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0d111-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d111-110">PARAMETERS</span></span>

### <span data-ttu-id="0d111-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d111-111">-DefaultProfile</span></span>
<span data-ttu-id="0d111-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d111-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d111-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0d111-113">-Force</span></span>
<span data-ttu-id="0d111-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0d111-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0d111-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d111-115">-Name</span></span>
<span data-ttu-id="0d111-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0d111-116">The resource name.</span></span>

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

### <span data-ttu-id="0d111-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d111-117">-PassThru</span></span>
<span data-ttu-id="0d111-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0d111-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0d111-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d111-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d111-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0d111-120">The resource group name.</span></span>

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

### <span data-ttu-id="0d111-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d111-121">-Confirm</span></span>
<span data-ttu-id="0d111-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d111-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d111-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d111-123">-WhatIf</span></span>
<span data-ttu-id="0d111-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d111-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d111-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d111-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d111-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d111-126">CommonParameters</span></span>
<span data-ttu-id="0d111-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d111-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d111-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d111-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d111-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d111-129">INPUTS</span></span>

### <span data-ttu-id="0d111-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0d111-130">System.String</span></span>

## <span data-ttu-id="0d111-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d111-131">OUTPUTS</span></span>

### <span data-ttu-id="0d111-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="0d111-132">System.Object</span></span>

## <span data-ttu-id="0d111-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d111-133">NOTES</span></span>

## <span data-ttu-id="0d111-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d111-134">RELATED LINKS</span></span>

