---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 97ddf35b453b324cf04309afd3a90be185d43224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756622"
---
# <span data-ttu-id="ac455-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ac455-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="ac455-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac455-102">SYNOPSIS</span></span>
<span data-ttu-id="ac455-103">Tar bort VMAccess-tillägget från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ac455-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac455-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac455-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac455-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac455-105">DESCRIPTION</span></span>
<span data-ttu-id="ac455-106">Cmdleten **Remove-AzureRmVMAccessExtension** tar bort tillägget för virtuell dator åtkomst (VMAccess) från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ac455-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="ac455-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac455-107">EXAMPLES</span></span>

## <span data-ttu-id="ac455-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac455-108">PARAMETERS</span></span>

### <span data-ttu-id="ac455-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac455-109">-DefaultProfile</span></span>
<span data-ttu-id="ac455-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac455-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac455-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ac455-111">-Force</span></span>
<span data-ttu-id="ac455-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ac455-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ac455-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac455-113">-Name</span></span>
<span data-ttu-id="ac455-114">Anger namnet på tillägget som tas bort med denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac455-114">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac455-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac455-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac455-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ac455-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ac455-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="ac455-117">-VMName</span></span>
<span data-ttu-id="ac455-118">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ac455-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ac455-119">Denna cmdlet tar bort VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ac455-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac455-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac455-120">-Confirm</span></span>
<span data-ttu-id="ac455-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac455-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac455-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac455-122">-WhatIf</span></span>
<span data-ttu-id="ac455-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac455-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ac455-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac455-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac455-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac455-125">CommonParameters</span></span>
<span data-ttu-id="ac455-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac455-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac455-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac455-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac455-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac455-128">INPUTS</span></span>

## <span data-ttu-id="ac455-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac455-129">OUTPUTS</span></span>

## <span data-ttu-id="ac455-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac455-130">NOTES</span></span>

## <span data-ttu-id="ac455-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac455-131">RELATED LINKS</span></span>

[<span data-ttu-id="ac455-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ac455-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="ac455-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ac455-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="ac455-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="ac455-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
