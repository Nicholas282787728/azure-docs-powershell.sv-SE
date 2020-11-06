---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 10874ffbb0846765bfbeae06ae4522989280e428
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575003"
---
# <span data-ttu-id="c968f-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c968f-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="c968f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c968f-102">SYNOPSIS</span></span>
<span data-ttu-id="c968f-103">Hämtar information om AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="c968f-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c968f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c968f-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c968f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c968f-105">DESCRIPTION</span></span>
<span data-ttu-id="c968f-106">Cmdleten **Get-AzureRmVMAEMExtension** hämtar information om tillägget Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="c968f-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="c968f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c968f-107">EXAMPLES</span></span>

### <span data-ttu-id="c968f-108">Exempel 1: skaffa AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="c968f-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="c968f-109">Med det här kommandot får du information om AEM-tillägget för den virtuella datorn med namnet contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="c968f-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="c968f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c968f-110">PARAMETERS</span></span>

### <span data-ttu-id="c968f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c968f-111">-DefaultProfile</span></span>
<span data-ttu-id="c968f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c968f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c968f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c968f-113">-Name</span></span>
<span data-ttu-id="c968f-114">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c968f-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c968f-115">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="c968f-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="c968f-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="c968f-116">-OSType</span></span>
<span data-ttu-id="c968f-117">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="c968f-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="c968f-118">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="c968f-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="c968f-119">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="c968f-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="c968f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c968f-120">-ResourceGroupName</span></span>
<span data-ttu-id="c968f-121">Anger namnet på resurs gruppen för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c968f-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="c968f-122">Denna cmdlet hämtar information för AEM-tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c968f-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="c968f-123">-Status</span><span class="sxs-lookup"><span data-stu-id="c968f-123">-Status</span></span>
<span data-ttu-id="c968f-124">Anger att denna cmdlet endast får instans vyn för AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="c968f-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="c968f-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="c968f-125">-VMName</span></span>
<span data-ttu-id="c968f-126">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c968f-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c968f-127">Denna cmdlet hämtar information om AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="c968f-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="c968f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c968f-128">CommonParameters</span></span>
<span data-ttu-id="c968f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c968f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c968f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c968f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c968f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c968f-131">INPUTS</span></span>

## <span data-ttu-id="c968f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c968f-132">OUTPUTS</span></span>

## <span data-ttu-id="c968f-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c968f-133">NOTES</span></span>

## <span data-ttu-id="c968f-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c968f-134">RELATED LINKS</span></span>

[<span data-ttu-id="c968f-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c968f-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c968f-136">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c968f-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="c968f-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="c968f-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


