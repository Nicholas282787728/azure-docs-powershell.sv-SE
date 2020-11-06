---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMConfig.md
ms.openlocfilehash: 2022a8a830d868f412e505f23e65c4c297bea543
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585751"
---
# <span data-ttu-id="2370b-101">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="2370b-101">New-AzureRmVMConfig</span></span>

## <span data-ttu-id="2370b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2370b-102">SYNOPSIS</span></span>
<span data-ttu-id="2370b-103">Skapar ett konfigurerbart virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="2370b-103">Creates a configurable virtual machine object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2370b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2370b-104">SYNTAX</span></span>

```
New-AzureRmVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>]
 [[-LicenseType] <String>] [[-IdentityType] <ResourceIdentityType>] [-AssignIdentity] [-Zone <String[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2370b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2370b-105">DESCRIPTION</span></span>
<span data-ttu-id="2370b-106">Cmdleten **New-AzureRmVMConfig** skapar en konfigurerbar lokal virtuell dator för Azure.</span><span class="sxs-lookup"><span data-stu-id="2370b-106">The **New-AzureRmVMConfig** cmdlet creates a configurable local virtual machine object for Azure.</span></span>
<span data-ttu-id="2370b-107">Andra cmdletar kan användas för att konfigurera ett virtuellt dator objekt, till exempel set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface och set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="2370b-107">Other cmdlets can be used to configure a virtual machine object, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="2370b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2370b-108">EXAMPLES</span></span>

### <span data-ttu-id="2370b-109">Exempel 1: skapa ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="2370b-109">Example 1: Create a virtual machine object</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

<span data-ttu-id="2370b-110">Det första kommandot får den tillgänglighets uppsättning som heter AvailablitySet03 i resurs gruppen som heter ResourceGroup11 och lagrar sedan objektet i $AvailabilitySet variabel.</span><span class="sxs-lookup"><span data-stu-id="2370b-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="2370b-111">Det andra kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="2370b-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2370b-112">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="2370b-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2370b-113">Den virtuella datorn tillhör den tillgänglighets uppsättning som lagras i $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2370b-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

## <span data-ttu-id="2370b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2370b-114">PARAMETERS</span></span>

### <span data-ttu-id="2370b-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2370b-115">-AssignIdentity</span></span>
<span data-ttu-id="2370b-116">Ange systemets tilldelade identitet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2370b-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2370b-117">-AvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="2370b-117">-AvailabilitySetId</span></span>
<span data-ttu-id="2370b-118">Anger ID för en tillgänglighets uppsättning.</span><span class="sxs-lookup"><span data-stu-id="2370b-118">Specifies the ID of an availability set.</span></span>
<span data-ttu-id="2370b-119">Om du vill hämta ett objekt med tillgänglighets uppsättning kan du använda Get-AzureRmAvailabilitySet cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2370b-119">To obtain an availability set object, use the Get-AzureRmAvailabilitySet cmdlet.</span></span>
<span data-ttu-id="2370b-120">Objektet tillgänglighet innehåller egenskapen ID.</span><span class="sxs-lookup"><span data-stu-id="2370b-120">The availability set object contains an ID property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2370b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2370b-121">-DefaultProfile</span></span>
<span data-ttu-id="2370b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2370b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2370b-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2370b-123">-IdentityType</span></span>
<span data-ttu-id="2370b-124">Identiteten för den virtuella datorn, om den är konfigurerad.</span><span class="sxs-lookup"><span data-stu-id="2370b-124">The identity of the virtual machine, if configured.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2370b-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2370b-125">-LicenseType</span></span>
<span data-ttu-id="2370b-126">Licens typen, som är till för att sätta ditt eget licens scenario.</span><span class="sxs-lookup"><span data-stu-id="2370b-126">The license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2370b-127">-Taggar</span><span class="sxs-lookup"><span data-stu-id="2370b-127">-Tags</span></span>
<span data-ttu-id="2370b-128">De taggar som är kopplade till resursen.</span><span class="sxs-lookup"><span data-stu-id="2370b-128">The tags attached to the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2370b-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="2370b-129">-VMName</span></span>
<span data-ttu-id="2370b-130">Anger ett namn för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2370b-130">Specifies a name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2370b-131">-VMSize</span><span class="sxs-lookup"><span data-stu-id="2370b-131">-VMSize</span></span>
<span data-ttu-id="2370b-132">Anger storleken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2370b-132">Specifies the size for the virtual machine.</span></span>

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

### <span data-ttu-id="2370b-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="2370b-133">-Zone</span></span>
<span data-ttu-id="2370b-134">Anger zon listan för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="2370b-134">Specifies the zone list for the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2370b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2370b-135">CommonParameters</span></span>
<span data-ttu-id="2370b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2370b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2370b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2370b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2370b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2370b-138">INPUTS</span></span>

## <span data-ttu-id="2370b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2370b-139">OUTPUTS</span></span>

## <span data-ttu-id="2370b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2370b-140">NOTES</span></span>

## <span data-ttu-id="2370b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2370b-141">RELATED LINKS</span></span>

[<span data-ttu-id="2370b-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2370b-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="2370b-143">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="2370b-143">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="2370b-144">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="2370b-144">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="2370b-145">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2370b-145">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)


