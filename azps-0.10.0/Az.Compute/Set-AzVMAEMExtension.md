---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: 87d7ff04b62bcee2e735dacbbdd9ddb3ab04d425
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924834"
---
# <span data-ttu-id="d1562-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1562-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="d1562-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1562-102">SYNOPSIS</span></span>
<span data-ttu-id="d1562-103">Aktiverar support för övervakning för SAP-system.</span><span class="sxs-lookup"><span data-stu-id="d1562-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="d1562-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1562-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1562-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1562-105">DESCRIPTION</span></span>
<span data-ttu-id="d1562-106">Cmdleten **set-AzVMAEMExtension** uppdaterar konfigurationen av en virtuell dator för att aktivera eller uppdatera supporten för övervakning för SAP-system som är installerade på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d1562-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="d1562-107">Denna cmdlet installerar den AEM-anknytning (Azure Enhanced Monitoring) som samlar in prestanda data och gör det synligt för SAP-systemet.</span><span class="sxs-lookup"><span data-stu-id="d1562-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="d1562-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1562-108">EXAMPLES</span></span>

### <span data-ttu-id="d1562-109">Exempel 1: använda AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="d1562-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="d1562-110">Det här kommandot konfigurerar den virtuella datorn som heter Contoso-server att använda AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="d1562-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="d1562-111">Kommandot anger lagrings kontot som heter stdstorage.</span><span class="sxs-lookup"><span data-stu-id="d1562-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="d1562-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1562-112">PARAMETERS</span></span>

### <span data-ttu-id="d1562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1562-113">-DefaultProfile</span></span>
<span data-ttu-id="d1562-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1562-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1562-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="d1562-115">-DisableWAD</span></span>
<span data-ttu-id="d1562-116">Anger att denna cmdlet inte aktiverar Azure Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d1562-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="d1562-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="d1562-117">-EnableWAD</span></span>
<span data-ttu-id="d1562-118">Om den här parametern tillhandahålls aktiverar cmdleten Windows Azure Diagnostics för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d1562-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="d1562-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="d1562-119">-OSType</span></span>
<span data-ttu-id="d1562-120">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="d1562-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="d1562-121">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="d1562-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="d1562-122">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="d1562-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="d1562-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1562-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1562-124">Anger namnet på resurs gruppen för den virtuella datorn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d1562-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d1562-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="d1562-125">-SkipStorage</span></span>
<span data-ttu-id="d1562-126">Anger att denna cmdlet hoppar över konfigurering av lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="d1562-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="d1562-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="d1562-127">-VMName</span></span>
<span data-ttu-id="d1562-128">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d1562-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d1562-129">Denna cmdlet lägger till AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d1562-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1562-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d1562-130">-WADStorageAccountName</span></span>
<span data-ttu-id="d1562-131">Anger namnet på det lagrings konto som används i cmdleten för att konfigurera LinuxDiagnostics-eller IaaSDiagnostics-tillägget.</span><span class="sxs-lookup"><span data-stu-id="d1562-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="d1562-132">Om den virtuella datorn inte använder ett standard lagrings konto måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="d1562-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="d1562-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1562-133">CommonParameters</span></span>
<span data-ttu-id="d1562-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1562-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1562-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1562-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1562-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1562-136">INPUTS</span></span>

### <span data-ttu-id="d1562-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="d1562-137">None</span></span>
<span data-ttu-id="d1562-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d1562-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1562-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1562-139">OUTPUTS</span></span>

### <span data-ttu-id="d1562-140">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d1562-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d1562-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1562-141">NOTES</span></span>

## <span data-ttu-id="d1562-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1562-142">RELATED LINKS</span></span>

[<span data-ttu-id="d1562-143">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1562-143">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="d1562-144">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1562-144">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="d1562-145">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="d1562-145">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


