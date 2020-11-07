---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: 01eb8cba77177ca35f2e1b73ec410baa44e4a58c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929073"
---
# <span data-ttu-id="4c82e-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4c82e-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="4c82e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c82e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c82e-103">Aktiverar support för övervakning för SAP-system.</span><span class="sxs-lookup"><span data-stu-id="4c82e-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c82e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c82e-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c82e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c82e-105">DESCRIPTION</span></span>
<span data-ttu-id="4c82e-106">Cmdleten **set-AzureRmVMAEMExtension** uppdaterar konfigurationen av en virtuell dator för att aktivera eller uppdatera supporten för övervakning för SAP-system som är installerade på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4c82e-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="4c82e-107">Denna cmdlet installerar den AEM-anknytning (Azure Enhanced Monitoring) som samlar in prestanda data och gör det synligt för SAP-systemet.</span><span class="sxs-lookup"><span data-stu-id="4c82e-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="4c82e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c82e-108">EXAMPLES</span></span>

### <span data-ttu-id="4c82e-109">Exempel 1: använda AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="4c82e-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="4c82e-110">Det här kommandot konfigurerar den virtuella datorn som heter Contoso-server att använda AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="4c82e-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="4c82e-111">Kommandot anger lagrings kontot som heter stdstorage.</span><span class="sxs-lookup"><span data-stu-id="4c82e-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="4c82e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c82e-112">PARAMETERS</span></span>

### <span data-ttu-id="4c82e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c82e-113">-DefaultProfile</span></span>
<span data-ttu-id="4c82e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c82e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c82e-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="4c82e-115">-DisableWAD</span></span>
<span data-ttu-id="4c82e-116">Anger att denna cmdlet inte aktiverar Azure Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4c82e-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="4c82e-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="4c82e-117">-EnableWAD</span></span>
<span data-ttu-id="4c82e-118">Om den här parametern tillhandahålls aktiverar cmdleten Windows Azure Diagnostics för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="4c82e-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c82e-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="4c82e-119">-OSType</span></span>
<span data-ttu-id="4c82e-120">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="4c82e-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="4c82e-121">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="4c82e-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="4c82e-122">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="4c82e-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c82e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c82e-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c82e-124">Anger namnet på resurs gruppen för den virtuella datorn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4c82e-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c82e-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="4c82e-125">-SkipStorage</span></span>
<span data-ttu-id="4c82e-126">Anger att denna cmdlet hoppar över konfigurering av lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="4c82e-126">Indicates that this cmdlet skips configuration of storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c82e-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="4c82e-127">-VMName</span></span>
<span data-ttu-id="4c82e-128">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4c82e-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4c82e-129">Denna cmdlet lägger till AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="4c82e-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c82e-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4c82e-130">-WADStorageAccountName</span></span>
<span data-ttu-id="4c82e-131">Anger namnet på det lagrings konto som används i cmdleten för att konfigurera LinuxDiagnostics-eller IaaSDiagnostics-tillägget.</span><span class="sxs-lookup"><span data-stu-id="4c82e-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="4c82e-132">Om den virtuella datorn inte använder ett standard lagrings konto måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="4c82e-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c82e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c82e-133">CommonParameters</span></span>
<span data-ttu-id="4c82e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c82e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c82e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c82e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c82e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c82e-136">INPUTS</span></span>

### <span data-ttu-id="4c82e-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="4c82e-137">None</span></span>
<span data-ttu-id="4c82e-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4c82e-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c82e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c82e-139">OUTPUTS</span></span>

### <span data-ttu-id="4c82e-140">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4c82e-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4c82e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c82e-141">NOTES</span></span>

## <span data-ttu-id="4c82e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c82e-142">RELATED LINKS</span></span>

[<span data-ttu-id="4c82e-143">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4c82e-143">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4c82e-144">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4c82e-144">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="4c82e-145">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4c82e-145">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


