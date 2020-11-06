---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: 931ed484850654ecebc368ced0b378ce2a40944f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573675"
---
# <span data-ttu-id="6f8ae-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6f8ae-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="6f8ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6f8ae-103">Aktiverar support för övervakning för SAP-system.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f8ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f8ae-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f8ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f8ae-105">DESCRIPTION</span></span>
<span data-ttu-id="6f8ae-106">Cmdleten **set-AzureRmVMAEMExtension** uppdaterar konfigurationen av en virtuell dator för att aktivera eller uppdatera supporten för övervakning för SAP-system som är installerade på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="6f8ae-107">Denna cmdlet installerar den AEM-anknytning (Azure Enhanced Monitoring) som samlar in prestanda data och gör det synligt för SAP-systemet.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="6f8ae-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f8ae-108">EXAMPLES</span></span>

### <span data-ttu-id="6f8ae-109">Exempel 1: använda AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="6f8ae-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="6f8ae-110">Det här kommandot konfigurerar den virtuella datorn som heter Contoso-server att använda AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="6f8ae-111">Kommandot anger lagrings kontot som heter stdstorage.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="6f8ae-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f8ae-112">PARAMETERS</span></span>

### <span data-ttu-id="6f8ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f8ae-113">-DefaultProfile</span></span>
<span data-ttu-id="6f8ae-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f8ae-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="6f8ae-115">-DisableWAD</span></span>
<span data-ttu-id="6f8ae-116">Anger att denna cmdlet inte aktiverar Azure Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="6f8ae-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="6f8ae-117">-EnableWAD</span></span>
<span data-ttu-id="6f8ae-118">Om den här parametern tillhandahålls aktiverar cmdleten Windows Azure Diagnostics för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="6f8ae-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="6f8ae-119">-OSType</span></span>
<span data-ttu-id="6f8ae-120">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="6f8ae-121">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="6f8ae-122">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="6f8ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f8ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f8ae-124">Anger namnet på resurs gruppen för den virtuella datorn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6f8ae-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="6f8ae-125">-SkipStorage</span></span>
<span data-ttu-id="6f8ae-126">Anger att denna cmdlet hoppar över konfigurering av lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="6f8ae-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f8ae-127">-VMName</span></span>
<span data-ttu-id="6f8ae-128">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6f8ae-129">Denna cmdlet lägger till AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f8ae-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f8ae-130">-WADStorageAccountName</span></span>
<span data-ttu-id="6f8ae-131">Anger namnet på det lagrings konto som används i cmdleten för att konfigurera LinuxDiagnostics-eller IaaSDiagnostics-tillägget.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="6f8ae-132">Om den virtuella datorn inte använder ett standard lagrings konto måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="6f8ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f8ae-133">CommonParameters</span></span>
<span data-ttu-id="6f8ae-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f8ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f8ae-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f8ae-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f8ae-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f8ae-136">INPUTS</span></span>

## <span data-ttu-id="6f8ae-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f8ae-137">OUTPUTS</span></span>

## <span data-ttu-id="6f8ae-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f8ae-138">NOTES</span></span>

## <span data-ttu-id="6f8ae-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f8ae-139">RELATED LINKS</span></span>

[<span data-ttu-id="6f8ae-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6f8ae-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="6f8ae-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6f8ae-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="6f8ae-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="6f8ae-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


