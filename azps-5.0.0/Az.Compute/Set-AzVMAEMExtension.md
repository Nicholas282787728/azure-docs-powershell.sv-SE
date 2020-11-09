---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319708"
---
# <span data-ttu-id="0cd2f-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0cd2f-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="0cd2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cd2f-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd2f-103">Aktiverar support för övervakning för SAP-system.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="0cd2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cd2f-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd2f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cd2f-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd2f-106">Cmdleten **set-AzVMAEMExtension** uppdaterar konfigurationen av en virtuell dator för att aktivera eller uppdatera supporten för övervakning för SAP-system som är installerade på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="0cd2f-107">Denna cmdlet installerar den AEM-anknytning (Azure Enhanced Monitoring) som samlar in prestanda data och gör det synligt för SAP-systemet.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="0cd2f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cd2f-108">EXAMPLES</span></span>

### <span data-ttu-id="0cd2f-109">Exempel 1: använda AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="0cd2f-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="0cd2f-110">Det här kommandot konfigurerar den virtuella datorn som heter Contoso-server att använda AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="0cd2f-111">Kommandot anger lagrings kontot som heter stdstorage.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="0cd2f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cd2f-112">PARAMETERS</span></span>

### <span data-ttu-id="0cd2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd2f-113">-DefaultProfile</span></span>
<span data-ttu-id="0cd2f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cd2f-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="0cd2f-115">-EnableWAD</span></span>
<span data-ttu-id="0cd2f-116">Om den här parametern tillhandahålls aktiverar cmdleten Windows Azure Diagnostics för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="0cd2f-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="0cd2f-117">-InstallNewExtension</span></span>
<span data-ttu-id="0cd2f-118">Installera den nya virtuella dator tillägget för SAP.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd2f-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0cd2f-119">-NoWait</span></span>
<span data-ttu-id="0cd2f-120">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0cd2f-121">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0cd2f-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="0cd2f-122">-OSType</span></span>
<span data-ttu-id="0cd2f-123">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0cd2f-124">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0cd2f-125">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="0cd2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0cd2f-127">Anger namnet på resurs gruppen för den virtuella datorn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0cd2f-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="0cd2f-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="0cd2f-129">Ställer in åtkomst för den virtuella dator identiteten till de enskilda resurserna, till exempel data diskar i stället för hela resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd2f-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="0cd2f-130">-SkipStorage</span></span>
<span data-ttu-id="0cd2f-131">Anger att denna cmdlet hoppar över konfigurering av lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-131">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd2f-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="0cd2f-132">-VMName</span></span>
<span data-ttu-id="0cd2f-133">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0cd2f-134">Denna cmdlet lägger till AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0cd2f-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0cd2f-135">-WADStorageAccountName</span></span>
<span data-ttu-id="0cd2f-136">Anger namnet på det lagrings konto som används i cmdleten för att konfigurera LinuxDiagnostics-eller IaaSDiagnostics-tillägget.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="0cd2f-137">Om den virtuella datorn inte använder ett standard lagrings konto måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd2f-138">CommonParameters</span></span>
<span data-ttu-id="0cd2f-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd2f-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cd2f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd2f-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cd2f-141">INPUTS</span></span>

### <span data-ttu-id="0cd2f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0cd2f-142">System.String</span></span>

## <span data-ttu-id="0cd2f-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cd2f-143">OUTPUTS</span></span>

### <span data-ttu-id="0cd2f-144">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0cd2f-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0cd2f-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cd2f-145">NOTES</span></span>

## <span data-ttu-id="0cd2f-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cd2f-146">RELATED LINKS</span></span>

[<span data-ttu-id="0cd2f-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0cd2f-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="0cd2f-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0cd2f-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="0cd2f-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0cd2f-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


