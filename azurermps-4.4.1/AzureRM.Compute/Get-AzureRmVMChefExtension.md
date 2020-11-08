---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 2aa0c6516614adb5fae84e2d141cf1882de71628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758426"
---
# <span data-ttu-id="08e1f-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="08e1f-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="08e1f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="08e1f-103">Hämtar information om en kock-anknytning.</span><span class="sxs-lookup"><span data-stu-id="08e1f-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e1f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08e1f-104">SYNTAX</span></span>

### <span data-ttu-id="08e1f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="08e1f-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e1f-106">Windows</span><span class="sxs-lookup"><span data-stu-id="08e1f-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e1f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08e1f-107">DESCRIPTION</span></span>
<span data-ttu-id="08e1f-108">Cmdleten **Get-AzureVMChefExtension** hämtar information om en kock-anknytning som är installerad på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="08e1f-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="08e1f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08e1f-109">EXAMPLES</span></span>

### <span data-ttu-id="08e1f-110">Exempel 1: Hämta information om chefs tillägget för en virtuell Windows-dator-</span><span class="sxs-lookup"><span data-stu-id="08e1f-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="08e1f-111">Det här kommandot får chefs tillägget från en Windows-dator med namnet WindowsVM001 som tillhör resurs gruppen med namnet ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="08e1f-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="08e1f-112">Exempel 2: Hämta information om chefs tillägget för en virtuell dator i Linux</span><span class="sxs-lookup"><span data-stu-id="08e1f-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="08e1f-113">Det här kommandot får chefs tillägget från en virtuell dator med virtuella Linux namnet LinuxVM001 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="08e1f-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="08e1f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08e1f-114">PARAMETERS</span></span>

### <span data-ttu-id="08e1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e1f-115">-DefaultProfile</span></span>
<span data-ttu-id="08e1f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08e1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08e1f-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="08e1f-117">-Linux</span></span>
<span data-ttu-id="08e1f-118">Anger att denna cmdlet fungerar på en virtuell dator med Linux.</span><span class="sxs-lookup"><span data-stu-id="08e1f-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e1f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="08e1f-119">-Name</span></span>
<span data-ttu-id="08e1f-120">Anger namnet på chefs tillägget.</span><span class="sxs-lookup"><span data-stu-id="08e1f-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="08e1f-122">Anger namnet på den resurs grupp som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="08e1f-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="08e1f-123">-Status</span><span class="sxs-lookup"><span data-stu-id="08e1f-123">-Status</span></span>
<span data-ttu-id="08e1f-124">Anger att denna cmdlet endast får instans vyn av kock-tillägget.</span><span class="sxs-lookup"><span data-stu-id="08e1f-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1f-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="08e1f-125">-VMName</span></span>
<span data-ttu-id="08e1f-126">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="08e1f-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="08e1f-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="08e1f-127">-Windows</span></span>
<span data-ttu-id="08e1f-128">Anger att denna cmdlet är för en Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="08e1f-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e1f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e1f-129">CommonParameters</span></span>
<span data-ttu-id="08e1f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e1f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e1f-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e1f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e1f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08e1f-132">INPUTS</span></span>

## <span data-ttu-id="08e1f-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08e1f-133">OUTPUTS</span></span>

## <span data-ttu-id="08e1f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08e1f-134">NOTES</span></span>

## <span data-ttu-id="08e1f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08e1f-135">RELATED LINKS</span></span>

[<span data-ttu-id="08e1f-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="08e1f-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="08e1f-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="08e1f-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)

