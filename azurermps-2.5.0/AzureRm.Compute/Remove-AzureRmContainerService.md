---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930670"
---
# <span data-ttu-id="a9415-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a9415-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="a9415-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9415-102">SYNOPSIS</span></span>
<span data-ttu-id="a9415-103">Tar bort en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="a9415-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9415-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9415-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9415-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9415-105">DESCRIPTION</span></span>
<span data-ttu-id="a9415-106">Cmdleten **Remove-AzureRmContainerService** tar bort en behållar tjänst från ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="a9415-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="a9415-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9415-107">EXAMPLES</span></span>

### <span data-ttu-id="a9415-108">Exempel 1: ta bort en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="a9415-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="a9415-109">Det här kommandot tar bort behållar tjänsten med namnet CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="a9415-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="a9415-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9415-110">PARAMETERS</span></span>

### <span data-ttu-id="a9415-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9415-111">-AsJob</span></span>
<span data-ttu-id="a9415-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="a9415-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a9415-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9415-113">-DefaultProfile</span></span>
<span data-ttu-id="a9415-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9415-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9415-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a9415-115">-Force</span></span>
<span data-ttu-id="a9415-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a9415-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9415-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9415-117">-Name</span></span>
<span data-ttu-id="a9415-118">Anger namnet på den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a9415-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9415-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9415-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9415-120">Anger resurs gruppen för den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a9415-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9415-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9415-121">-Confirm</span></span>
<span data-ttu-id="a9415-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9415-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="a9415-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9415-123">-WhatIf</span></span>
<span data-ttu-id="a9415-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9415-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9415-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9415-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="a9415-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9415-126">CommonParameters</span></span>
<span data-ttu-id="a9415-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9415-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9415-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9415-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9415-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9415-129">INPUTS</span></span>

### <span data-ttu-id="a9415-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="a9415-130">None</span></span>
<span data-ttu-id="a9415-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a9415-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9415-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9415-132">OUTPUTS</span></span>

### <span data-ttu-id="a9415-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="a9415-133">System.Void</span></span>

## <span data-ttu-id="a9415-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9415-134">NOTES</span></span>

## <span data-ttu-id="a9415-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9415-135">RELATED LINKS</span></span>

[<span data-ttu-id="a9415-136">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a9415-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="a9415-137">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a9415-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="a9415-138">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a9415-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


