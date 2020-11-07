---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 5b2da41aff052805ac400001367d4d4a8f6abf18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575002"
---
# <span data-ttu-id="d2da5-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d2da5-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="d2da5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2da5-102">SYNOPSIS</span></span>
<span data-ttu-id="d2da5-103">Konfigurerar Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d2da5-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2da5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2da5-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2da5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2da5-105">DESCRIPTION</span></span>
<span data-ttu-id="d2da5-106">Cmdleten **set-AzureRmVMDiagnosticsExtension** konfigurerar Azure Diagnostics-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="d2da5-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="d2da5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2da5-107">EXAMPLES</span></span>

### <span data-ttu-id="d2da5-108">Exempel 1: Aktivera diagnostik med ett lagrings konto som angetts i en konfigurations fil för diagnostik</span><span class="sxs-lookup"><span data-stu-id="d2da5-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="d2da5-109">Med det här kommandot används en diagnostik-konfigurations fil för att aktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="d2da5-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="d2da5-110">Filen diagnostics_publicconfig.xml innehåller den offentliga XML-konfigurationen för diagnostikprogrammet, inklusive namnet på det lagrings konto som diagnostikdata ska skickas till.</span><span class="sxs-lookup"><span data-stu-id="d2da5-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="d2da5-111">Diagnostics Storage-kontot måste finnas i samma prenumeration som den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d2da5-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d2da5-112">Exempel 2: Aktivera diagnostik med ett lagrings konto namn</span><span class="sxs-lookup"><span data-stu-id="d2da5-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="d2da5-113">Det här kommandot använder lagrings konto namnet för att aktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="d2da5-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="d2da5-114">Om Diagnostics-konfigurationen inte anger ett lagrings konto namn eller om du vill åsidosätta namnet på diagnostik-kontot som angetts i konfigurations filen använder du parametern *StorageAccountName* .</span><span class="sxs-lookup"><span data-stu-id="d2da5-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="d2da5-115">Diagnostics Storage-kontot måste finnas i samma prenumeration som den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d2da5-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="d2da5-116">Exempel 3: Aktivera diagnostik med namn och nycklar för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="d2da5-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="d2da5-117">Det här kommandot använder namn och nycklar för lagrings kontot för att aktivera diagnostik.</span><span class="sxs-lookup"><span data-stu-id="d2da5-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="d2da5-118">Om Diagnostics Storage-kontot finns i ett annat abonnemang än den virtuella datorn aktiverar du det genom att uttryckligen ange dess namn och nycklar.</span><span class="sxs-lookup"><span data-stu-id="d2da5-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="d2da5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2da5-119">PARAMETERS</span></span>

### <span data-ttu-id="d2da5-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d2da5-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d2da5-121">Anger om den här cmdleten gör att Azure gästs agenten automatiskt kan uppdatera tillägget till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="d2da5-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="d2da5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2da5-122">-DefaultProfile</span></span>
<span data-ttu-id="d2da5-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d2da5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2da5-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="d2da5-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="d2da5-125">Anger sökvägen för konfigurations filen.</span><span class="sxs-lookup"><span data-stu-id="d2da5-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="d2da5-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="d2da5-126">-Location</span></span>
<span data-ttu-id="d2da5-127">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d2da5-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d2da5-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="d2da5-128">-Name</span></span>
<span data-ttu-id="d2da5-129">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="d2da5-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="d2da5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2da5-130">-ResourceGroupName</span></span>
<span data-ttu-id="d2da5-131">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d2da5-131">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d2da5-132">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2da5-132">-StorageAccountEndpoint</span></span>
<span data-ttu-id="d2da5-133">Anger slut punkt för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d2da5-133">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="d2da5-134">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d2da5-134">-StorageAccountKey</span></span>
<span data-ttu-id="d2da5-135">Anger lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d2da5-135">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="d2da5-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2da5-136">-StorageAccountName</span></span>
<span data-ttu-id="d2da5-137">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d2da5-137">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="d2da5-138">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d2da5-138">-StorageContext</span></span>
<span data-ttu-id="d2da5-139">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="d2da5-139">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="d2da5-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d2da5-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="d2da5-141">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d2da5-141">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="d2da5-142">För att hämta versionen kör du Get-AzureRmVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="d2da5-142">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="d2da5-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="d2da5-143">-VMName</span></span>
<span data-ttu-id="d2da5-144">Anger namnet på den virtuella dator där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="d2da5-144">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d2da5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2da5-145">CommonParameters</span></span>
<span data-ttu-id="d2da5-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2da5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2da5-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2da5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2da5-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2da5-148">INPUTS</span></span>

## <span data-ttu-id="d2da5-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2da5-149">OUTPUTS</span></span>

## <span data-ttu-id="d2da5-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2da5-150">NOTES</span></span>

## <span data-ttu-id="d2da5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2da5-151">RELATED LINKS</span></span>

[<span data-ttu-id="d2da5-152">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d2da5-152">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="d2da5-153">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="d2da5-153">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="d2da5-154">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="d2da5-154">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

