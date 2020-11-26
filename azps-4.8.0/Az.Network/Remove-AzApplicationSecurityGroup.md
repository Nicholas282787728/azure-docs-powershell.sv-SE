---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261832"
---
# <span data-ttu-id="314fd-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="314fd-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="314fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="314fd-102">SYNOPSIS</span></span>
<span data-ttu-id="314fd-103">Tar bort en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="314fd-103">Removes an application security group.</span></span>

## <span data-ttu-id="314fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="314fd-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="314fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="314fd-105">DESCRIPTION</span></span>
<span data-ttu-id="314fd-106">Cmdleten **Remove-AzApplicationSecurityGroup** tar bort en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="314fd-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="314fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="314fd-107">EXAMPLES</span></span>

### <span data-ttu-id="314fd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="314fd-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="314fd-109">Det här kommandot tar bort en säkerhets grupp för program med namnet MyApplicationSecurityGrouo i resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="314fd-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="314fd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="314fd-110">PARAMETERS</span></span>

### <span data-ttu-id="314fd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="314fd-111">-AsJob</span></span>
<span data-ttu-id="314fd-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="314fd-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314fd-113">-DefaultProfile</span></span>
<span data-ttu-id="314fd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="314fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="314fd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="314fd-115">-Force</span></span>
<span data-ttu-id="314fd-116">Fråga inte efter bekräftelse om du vill ta bort resursen</span><span class="sxs-lookup"><span data-stu-id="314fd-116">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314fd-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="314fd-117">-Name</span></span>
<span data-ttu-id="314fd-118">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="314fd-118">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="314fd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="314fd-119">-PassThru</span></span>
<span data-ttu-id="314fd-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="314fd-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="314fd-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="314fd-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="314fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="314fd-123">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="314fd-123">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="314fd-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="314fd-124">-Confirm</span></span>
<span data-ttu-id="314fd-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="314fd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314fd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="314fd-126">-WhatIf</span></span>
<span data-ttu-id="314fd-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="314fd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="314fd-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="314fd-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314fd-129">CommonParameters</span></span>
<span data-ttu-id="314fd-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314fd-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314fd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314fd-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="314fd-132">INPUTS</span></span>

### <span data-ttu-id="314fd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="314fd-133">System.String</span></span>

## <span data-ttu-id="314fd-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="314fd-134">OUTPUTS</span></span>

### <span data-ttu-id="314fd-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="314fd-135">System.Boolean</span></span>

## <span data-ttu-id="314fd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="314fd-136">NOTES</span></span>

## <span data-ttu-id="314fd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="314fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="314fd-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="314fd-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="314fd-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="314fd-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)