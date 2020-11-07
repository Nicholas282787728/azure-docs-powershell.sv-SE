---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: deaa8470a4af38eba1f38581e03165c19b3b18f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744958"
---
# <span data-ttu-id="0b234-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b234-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="0b234-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b234-102">SYNOPSIS</span></span>
<span data-ttu-id="0b234-103">Aktiverar support för övervakning för SAP-system.</span><span class="sxs-lookup"><span data-stu-id="0b234-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="0b234-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b234-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b234-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b234-105">DESCRIPTION</span></span>
<span data-ttu-id="0b234-106">Cmdleten **set-AzVMAEMExtension** uppdaterar konfigurationen av en virtuell dator för att aktivera eller uppdatera supporten för övervakning för SAP-system som är installerade på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0b234-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="0b234-107">Denna cmdlet installerar den AEM-anknytning (Azure Enhanced Monitoring) som samlar in prestanda data och gör det synligt för SAP-systemet.</span><span class="sxs-lookup"><span data-stu-id="0b234-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="0b234-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b234-108">EXAMPLES</span></span>

### <span data-ttu-id="0b234-109">Exempel 1: använda AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="0b234-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="0b234-110">Det här kommandot konfigurerar den virtuella datorn som heter Contoso-server att använda AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="0b234-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="0b234-111">Kommandot anger lagrings kontot som heter stdstorage.</span><span class="sxs-lookup"><span data-stu-id="0b234-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="0b234-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b234-112">PARAMETERS</span></span>

### <span data-ttu-id="0b234-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b234-113">-DefaultProfile</span></span>
<span data-ttu-id="0b234-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b234-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b234-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="0b234-115">-EnableWAD</span></span>
<span data-ttu-id="0b234-116">Om den här parametern tillhandahålls aktiverar cmdleten Windows Azure Diagnostics för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0b234-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="0b234-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0b234-117">-NoWait</span></span>
<span data-ttu-id="0b234-118">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="0b234-118">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0b234-119">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="0b234-119">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0b234-120">-OSType</span><span class="sxs-lookup"><span data-stu-id="0b234-120">-OSType</span></span>
<span data-ttu-id="0b234-121">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="0b234-121">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0b234-122">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="0b234-122">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0b234-123">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="0b234-123">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="0b234-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b234-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b234-125">Anger namnet på resurs gruppen för den virtuella datorn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="0b234-125">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0b234-126">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="0b234-126">-SkipStorage</span></span>
<span data-ttu-id="0b234-127">Anger att denna cmdlet hoppar över konfigurering av lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="0b234-127">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="0b234-128">-VMName</span><span class="sxs-lookup"><span data-stu-id="0b234-128">-VMName</span></span>
<span data-ttu-id="0b234-129">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0b234-129">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0b234-130">Denna cmdlet lägger till AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0b234-130">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0b234-131">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0b234-131">-WADStorageAccountName</span></span>
<span data-ttu-id="0b234-132">Anger namnet på det lagrings konto som används i cmdleten för att konfigurera LinuxDiagnostics-eller IaaSDiagnostics-tillägget.</span><span class="sxs-lookup"><span data-stu-id="0b234-132">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="0b234-133">Om den virtuella datorn inte använder ett standard lagrings konto måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="0b234-133">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="0b234-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b234-134">CommonParameters</span></span>
<span data-ttu-id="0b234-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b234-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b234-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b234-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b234-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b234-137">INPUTS</span></span>

### <span data-ttu-id="0b234-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0b234-138">System.String</span></span>

## <span data-ttu-id="0b234-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b234-139">OUTPUTS</span></span>

### <span data-ttu-id="0b234-140">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0b234-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0b234-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b234-141">NOTES</span></span>

## <span data-ttu-id="0b234-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b234-142">RELATED LINKS</span></span>

[<span data-ttu-id="0b234-143">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b234-143">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="0b234-144">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b234-144">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="0b234-145">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0b234-145">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)

