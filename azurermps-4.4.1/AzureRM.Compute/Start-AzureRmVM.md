---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574731"
---
# <span data-ttu-id="f54be-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f54be-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="f54be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f54be-102">SYNOPSIS</span></span>
<span data-ttu-id="f54be-103">Startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="f54be-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f54be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f54be-104">SYNTAX</span></span>

### <span data-ttu-id="f54be-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="f54be-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f54be-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f54be-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f54be-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f54be-107">DESCRIPTION</span></span>
<span data-ttu-id="f54be-108">Cmdleten **Start-AzureRmVM** startar en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="f54be-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f54be-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f54be-109">EXAMPLES</span></span>

### <span data-ttu-id="f54be-110">Exempel 1: starta en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="f54be-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f54be-111">Det här kommandot startar den virtuella datorn med namnet VirtualMachine07 i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f54be-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="f54be-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f54be-112">PARAMETERS</span></span>

### <span data-ttu-id="f54be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54be-113">-DefaultProfile</span></span>
<span data-ttu-id="f54be-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f54be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f54be-115">-ID</span><span class="sxs-lookup"><span data-stu-id="f54be-115">-Id</span></span>
<span data-ttu-id="f54be-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f54be-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54be-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f54be-117">-Name</span></span>
<span data-ttu-id="f54be-118">Den virtuella datorns namn.</span><span class="sxs-lookup"><span data-stu-id="f54be-118">The virtual machine name.</span></span>

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

### <span data-ttu-id="f54be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f54be-119">-ResourceGroupName</span></span>
<span data-ttu-id="f54be-120">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f54be-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f54be-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f54be-121">-Confirm</span></span>
<span data-ttu-id="f54be-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f54be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f54be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f54be-123">-WhatIf</span></span>
<span data-ttu-id="f54be-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f54be-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f54be-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f54be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f54be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54be-126">CommonParameters</span></span>
<span data-ttu-id="f54be-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54be-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f54be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54be-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f54be-129">INPUTS</span></span>

## <span data-ttu-id="f54be-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f54be-130">OUTPUTS</span></span>

## <span data-ttu-id="f54be-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f54be-131">NOTES</span></span>

## <span data-ttu-id="f54be-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f54be-132">RELATED LINKS</span></span>

[<span data-ttu-id="f54be-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f54be-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f54be-134">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f54be-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="f54be-135">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f54be-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="f54be-136">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f54be-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="f54be-137">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f54be-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="f54be-138">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f54be-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


