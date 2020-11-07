---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: e79229053030fdd2c1ed8a8fae4fccee493972a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754459"
---
# <span data-ttu-id="7d0c3-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7d0c3-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="7d0c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="7d0c3-103">Konfigurerar Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="7d0c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d0c3-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d0c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d0c3-105">DESCRIPTION</span></span>
<span data-ttu-id="7d0c3-106">Cmdleten **set-AzVMDiagnosticsExtension** konfigurerar Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="7d0c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d0c3-107">EXAMPLES</span></span>

### <span data-ttu-id="7d0c3-108">Exempel 1: Aktivera diagnostik med ett lagrings konto som angetts i en konfigurations fil för diagnostik</span><span class="sxs-lookup"><span data-stu-id="7d0c3-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="7d0c3-109">Med det här kommandot används en diagnostik-konfigurations fil för att aktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="7d0c3-110">Filen diagnostics_publicconfig.xml innehåller den offentliga XML-konfigurationen för diagnostikprogrammet, inklusive namnet på det lagrings konto som diagnostikdata ska skickas till.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="7d0c3-111">Diagnostics Storage-kontot måste finnas i samma prenumeration som den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="7d0c3-112">Exempel 2: Aktivera diagnostik med ett lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="7d0c3-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="7d0c3-113">Det här kommandot använder lagrings konto namnet för att aktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="7d0c3-114">Om Diagnostics-konfigurationen inte anger ett lagrings konto namn eller om du vill åsidosätta namnet på diagnostik-kontot som angetts i konfigurations filen använder du parametern *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="7d0c3-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="7d0c3-115">Diagnostics Storage-kontot måste finnas i samma prenumeration som den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="7d0c3-116">Exempel 3: Aktivera diagnostik med namn och nycklar för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="7d0c3-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="7d0c3-117">Det här kommandot använder namn och nycklar för lagrings kontot för att aktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="7d0c3-118">Om Diagnostics Storage-kontot finns i ett annat abonnemang än den virtuella datorn aktiverar du det genom att uttryckligen ange dess namn och nycklar.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="7d0c3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d0c3-119">PARAMETERS</span></span>

### <span data-ttu-id="7d0c3-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7d0c3-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7d0c3-121">Anger om den här cmdleten gör att Azure gästs agenten automatiskt kan uppdatera tillägget till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d0c3-122">-DefaultProfile</span></span>
<span data-ttu-id="7d0c3-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d0c3-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="7d0c3-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="7d0c3-125">Anger sökvägen för konfigurations filen.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="7d0c3-126">-Location</span></span>
<span data-ttu-id="7d0c3-127">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d0c3-128">-Name</span></span>
<span data-ttu-id="7d0c3-129">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d0c3-130">-ResourceGroupName</span></span>
<span data-ttu-id="7d0c3-131">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-131">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7d0c3-132">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d0c3-132">-StorageAccountEndpoint</span></span>
<span data-ttu-id="7d0c3-133">Anger slut punkt för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-133">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-134">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7d0c3-134">-StorageAccountKey</span></span>
<span data-ttu-id="7d0c3-135">Anger lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-135">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7d0c3-136">-StorageAccountName</span></span>
<span data-ttu-id="7d0c3-137">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-137">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-138">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="7d0c3-138">-StorageContext</span></span>
<span data-ttu-id="7d0c3-139">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-139">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7d0c3-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="7d0c3-141">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-141">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="7d0c3-142">För att hämta versionen kör du Get-AzVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="7d0c3-142">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0c3-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="7d0c3-143">-VMName</span></span>
<span data-ttu-id="7d0c3-144">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-144">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7d0c3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0c3-145">CommonParameters</span></span>
<span data-ttu-id="7d0c3-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d0c3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0c3-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d0c3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0c3-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d0c3-148">INPUTS</span></span>

### <span data-ttu-id="7d0c3-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7d0c3-149">System.String</span></span>

### <span data-ttu-id="7d0c3-150">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d0c3-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="7d0c3-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d0c3-151">System.Boolean</span></span>

## <span data-ttu-id="7d0c3-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d0c3-152">OUTPUTS</span></span>

### <span data-ttu-id="7d0c3-153">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7d0c3-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7d0c3-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d0c3-154">NOTES</span></span>

## <span data-ttu-id="7d0c3-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d0c3-155">RELATED LINKS</span></span>

[<span data-ttu-id="7d0c3-156">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7d0c3-156">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="7d0c3-157">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="7d0c3-157">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="7d0c3-158">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7d0c3-158">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


