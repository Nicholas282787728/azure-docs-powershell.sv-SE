---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: f0380a518353c3bc462a8a7b58012871359569a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576330"
---
# <span data-ttu-id="6ead1-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="6ead1-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="6ead1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ead1-102">SYNOPSIS</span></span>
<span data-ttu-id="6ead1-103">Hämtar objekten under en behållare i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="6ead1-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ead1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ead1-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ead1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ead1-105">DESCRIPTION</span></span>
<span data-ttu-id="6ead1-106">Cmdleten **Get-AzureRmBackupItem** hämtar objekten i en behållare i Azure Backup och objektets skydds status.</span><span class="sxs-lookup"><span data-stu-id="6ead1-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="6ead1-107">Aktivera objekt för skydd med hjälp av Enable-AzureRmBackupProtection cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ead1-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>
<span data-ttu-id="6ead1-108">En behållare som är registrerad för ett säkerhets kopierings valv kan innehålla ett eller flera objekt som kan skyddas.</span><span class="sxs-lookup"><span data-stu-id="6ead1-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="6ead1-109">För virtuella Azure-datorer kan det bara finnas ett objekt i behållaren virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6ead1-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="6ead1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ead1-110">EXAMPLES</span></span>

### <span data-ttu-id="6ead1-111">Exempel 1: Hämta objekten i en behållare</span><span class="sxs-lookup"><span data-stu-id="6ead1-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="6ead1-112">Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ead1-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="6ead1-113">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="6ead1-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="6ead1-114">Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="6ead1-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="6ead1-115">Kommandot lagrar objektet i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="6ead1-115">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="6ead1-116">Det slutliga kommandot hämtar säkerhets kopian i behållaren i $Container.</span><span class="sxs-lookup"><span data-stu-id="6ead1-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="6ead1-117">Exempel 2: Visa alla egenskaper för ett objekt</span><span class="sxs-lookup"><span data-stu-id="6ead1-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="6ead1-118">Det här kommandot får säkerhets kopian i behållaren i $Container och skickar den sedan till Select-Object cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ead1-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="6ead1-119">Denna cmdlet returnerar alla egenskaper för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="6ead1-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="6ead1-120">Om du vill ha mer information skriver du `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="6ead1-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="6ead1-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ead1-121">PARAMETERS</span></span>

### <span data-ttu-id="6ead1-122">-Container</span><span class="sxs-lookup"><span data-stu-id="6ead1-122">-Container</span></span>
<span data-ttu-id="6ead1-123">Anger ett Container-objekt som denna cmdlet ska säkerhetskopiera objekt för.</span><span class="sxs-lookup"><span data-stu-id="6ead1-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="6ead1-124">För att få en **AzureRmBackupContainer** , Använd cmdleten Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="6ead1-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ead1-125">-DefaultProfile</span></span>
<span data-ttu-id="6ead1-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6ead1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ead1-127">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="6ead1-127">-ProtectionStatus</span></span>
<span data-ttu-id="6ead1-128">Anger det allmänna skydds statusvärdet för ett objekt i behållaren.</span><span class="sxs-lookup"><span data-stu-id="6ead1-128">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="6ead1-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6ead1-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6ead1-130">Upphovsrättsskydd</span><span class="sxs-lookup"><span data-stu-id="6ead1-130">Protected</span></span> 
- <span data-ttu-id="6ead1-131">Lösenordsskydd</span><span class="sxs-lookup"><span data-stu-id="6ead1-131">Protecting</span></span>  
- <span data-ttu-id="6ead1-132">NotProtected</span><span class="sxs-lookup"><span data-stu-id="6ead1-132">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ead1-133">-Status</span><span class="sxs-lookup"><span data-stu-id="6ead1-133">-Status</span></span>
<span data-ttu-id="6ead1-134">Anger säkerhets kopians status för ett objekt.</span><span class="sxs-lookup"><span data-stu-id="6ead1-134">Specifies the backup status for an item.</span></span>
<span data-ttu-id="6ead1-135">De acceptabla värdena för den här parametern är: IRPending, protected, ProtectionError och ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="6ead1-135">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="6ead1-136">Om parametern *ProtectionStatus* har värdet skyddat kan du använda värdet för kommandot *status* för att filtrera objekt.</span><span class="sxs-lookup"><span data-stu-id="6ead1-136">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ead1-137">– Skriv</span><span class="sxs-lookup"><span data-stu-id="6ead1-137">-Type</span></span>
<span data-ttu-id="6ead1-138">Anger den typ av objekt som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6ead1-138">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="6ead1-139">För närvarande är det enda värdet som stöds AzureVM.</span><span class="sxs-lookup"><span data-stu-id="6ead1-139">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ead1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ead1-140">CommonParameters</span></span>
<span data-ttu-id="6ead1-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ead1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ead1-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ead1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ead1-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ead1-143">INPUTS</span></span>

### <span data-ttu-id="6ead1-144">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6ead1-144">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="6ead1-145">Parametrar: container (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ead1-145">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="6ead1-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ead1-146">OUTPUTS</span></span>

### <span data-ttu-id="6ead1-147">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="6ead1-147">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>

## <span data-ttu-id="6ead1-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ead1-148">NOTES</span></span>

## <span data-ttu-id="6ead1-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ead1-149">RELATED LINKS</span></span>

[<span data-ttu-id="6ead1-150">Säkerhets kopiering-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="6ead1-150">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="6ead1-151">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6ead1-151">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="6ead1-152">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6ead1-152">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="6ead1-153">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6ead1-153">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="6ead1-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="6ead1-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="6ead1-155">Återställ-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="6ead1-155">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


