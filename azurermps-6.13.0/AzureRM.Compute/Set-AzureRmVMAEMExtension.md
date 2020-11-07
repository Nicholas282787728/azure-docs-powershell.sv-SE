---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: c006c06d03e1f1c120ed62f38ea8b3e451d8fa21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757902"
---
# <span data-ttu-id="b6a8a-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6a8a-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="b6a8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a8a-103">Aktiverar support för övervakning för SAP-system.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6a8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6a8a-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a8a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a8a-106">Cmdleten **set-AzureRmVMAEMExtension** uppdaterar konfigurationen av en virtuell dator för att aktivera eller uppdatera supporten för övervakning för SAP-system som är installerade på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="b6a8a-107">Denna cmdlet installerar den AEM-anknytning (Azure Enhanced Monitoring) som samlar in prestanda data och gör det synligt för SAP-systemet.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="b6a8a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6a8a-108">EXAMPLES</span></span>

### <span data-ttu-id="b6a8a-109">Exempel 1: använda AEM-tillägget</span><span class="sxs-lookup"><span data-stu-id="b6a8a-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="b6a8a-110">Det här kommandot konfigurerar den virtuella datorn som heter Contoso-server att använda AEM-tillägget.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="b6a8a-111">Kommandot anger lagrings kontot som heter stdstorage.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="b6a8a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6a8a-112">PARAMETERS</span></span>

### <span data-ttu-id="b6a8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a8a-113">-DefaultProfile</span></span>
<span data-ttu-id="b6a8a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a8a-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="b6a8a-115">-EnableWAD</span></span>
<span data-ttu-id="b6a8a-116">Om den här parametern tillhandahålls aktiverar cmdleten Windows Azure Diagnostics för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="b6a8a-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="b6a8a-117">-OSType</span></span>
<span data-ttu-id="b6a8a-118">Visar operativ systemets operativ system.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-118">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="b6a8a-119">Om operativ system disken inte har en typ måste du ange den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-119">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="b6a8a-120">De acceptabla värdena för denna parameter är: Windows och Linux.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-120">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="b6a8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="b6a8a-122">Anger namnet på resurs gruppen för den virtuella datorn som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-122">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b6a8a-123">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="b6a8a-123">-SkipStorage</span></span>
<span data-ttu-id="b6a8a-124">Anger att denna cmdlet hoppar över konfigurering av lagrings utrymme.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-124">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="b6a8a-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="b6a8a-125">-VMName</span></span>
<span data-ttu-id="b6a8a-126">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b6a8a-127">Denna cmdlet lägger till AEM-tillägget för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-127">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6a8a-128">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b6a8a-128">-WADStorageAccountName</span></span>
<span data-ttu-id="b6a8a-129">Anger namnet på det lagrings konto som används i cmdleten för att konfigurera LinuxDiagnostics-eller IaaSDiagnostics-tillägget.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-129">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="b6a8a-130">Om den virtuella datorn inte använder ett standard lagrings konto måste du ange ett värde för den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-130">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="b6a8a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a8a-131">CommonParameters</span></span>
<span data-ttu-id="b6a8a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a8a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a8a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a8a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a8a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6a8a-134">INPUTS</span></span>

### <span data-ttu-id="b6a8a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a8a-135">System.String</span></span>

## <span data-ttu-id="b6a8a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6a8a-136">OUTPUTS</span></span>

### <span data-ttu-id="b6a8a-137">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b6a8a-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b6a8a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6a8a-138">NOTES</span></span>

## <span data-ttu-id="b6a8a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6a8a-139">RELATED LINKS</span></span>

[<span data-ttu-id="b6a8a-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6a8a-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="b6a8a-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6a8a-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="b6a8a-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b6a8a-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


