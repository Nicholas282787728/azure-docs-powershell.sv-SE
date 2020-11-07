---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930069"
---
# <span data-ttu-id="207b0-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="207b0-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="207b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="207b0-102">SYNOPSIS</span></span>
<span data-ttu-id="207b0-103">Får ett resurs lås.</span><span class="sxs-lookup"><span data-stu-id="207b0-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="207b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="207b0-104">SYNTAX</span></span>

### <span data-ttu-id="207b0-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="207b0-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="207b0-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="207b0-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="207b0-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="207b0-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="207b0-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="207b0-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="207b0-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="207b0-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="207b0-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="207b0-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="207b0-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="207b0-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="207b0-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="207b0-112">DESCRIPTION</span></span>
<span data-ttu-id="207b0-113">Cmdleten **Get-AzureRmResourceLock** får Azure Resource lock.</span><span class="sxs-lookup"><span data-stu-id="207b0-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="207b0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="207b0-114">EXAMPLES</span></span>

### <span data-ttu-id="207b0-115">Exempel 1: skaffa ett lås</span><span class="sxs-lookup"><span data-stu-id="207b0-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="207b0-116">Det här kommandot får resurs låset med namnet ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="207b0-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="207b0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="207b0-117">PARAMETERS</span></span>

### <span data-ttu-id="207b0-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="207b0-118">-ApiVersion</span></span>
<span data-ttu-id="207b0-119">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="207b0-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="207b0-120">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="207b0-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="207b0-121">-AtScope</span></span>
<span data-ttu-id="207b0-122">Anger att denna cmdlet returnerar alla lås på eller ovanför det angivna omfånget.</span><span class="sxs-lookup"><span data-stu-id="207b0-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="207b0-123">Om du inte anger den här parametern returnerar cmdleten alla lås på, ovanför eller under scopet.</span><span class="sxs-lookup"><span data-stu-id="207b0-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="207b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="207b0-124">-DefaultProfile</span></span>
<span data-ttu-id="207b0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="207b0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="207b0-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="207b0-126">-InformationAction</span></span>
<span data-ttu-id="207b0-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="207b0-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="207b0-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="207b0-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="207b0-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="207b0-129">Continue</span></span>
- <span data-ttu-id="207b0-130">Över</span><span class="sxs-lookup"><span data-stu-id="207b0-130">Ignore</span></span>
- <span data-ttu-id="207b0-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="207b0-131">Inquire</span></span>
- <span data-ttu-id="207b0-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="207b0-132">SilentlyContinue</span></span>
- <span data-ttu-id="207b0-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="207b0-133">Stop</span></span>
- <span data-ttu-id="207b0-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="207b0-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="207b0-135">-InformationVariable</span></span>
<span data-ttu-id="207b0-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="207b0-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="207b0-137">-LockId</span></span>
<span data-ttu-id="207b0-138">Anger ID för det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="207b0-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-139">-LockName</span><span class="sxs-lookup"><span data-stu-id="207b0-139">-LockName</span></span>
<span data-ttu-id="207b0-140">Anger namnet på det lås som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="207b0-140">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-141">-För</span><span class="sxs-lookup"><span data-stu-id="207b0-141">-Pre</span></span>
<span data-ttu-id="207b0-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="207b0-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="207b0-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="207b0-143">-ResourceGroupName</span></span>
<span data-ttu-id="207b0-144">Anger namnet på den resurs grupp som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="207b0-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="207b0-145">Denna cmdlet hämtar lås för den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="207b0-145">This cmdlet gets locks for this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="207b0-146">-ResourceName</span></span>
<span data-ttu-id="207b0-147">Anger namnet på resursen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="207b0-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="207b0-148">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="207b0-148">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="207b0-149">-ResourceType</span></span>
<span data-ttu-id="207b0-150">Anger resurs typen för den resurs som den här låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="207b0-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="207b0-151">Denna cmdlet hämtar lås för den här resursen.</span><span class="sxs-lookup"><span data-stu-id="207b0-151">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-152">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="207b0-152">-Scope</span></span>
<span data-ttu-id="207b0-153">Anger omfattningen som låset gäller för.</span><span class="sxs-lookup"><span data-stu-id="207b0-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="207b0-154">Cmdleten får lås för detta scope.</span><span class="sxs-lookup"><span data-stu-id="207b0-154">The cmdlet gets locks for this scope.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="207b0-155">-TenantLevel</span></span>
<span data-ttu-id="207b0-156">Anger att denna cmdlet fungerar på klient nivån.</span><span class="sxs-lookup"><span data-stu-id="207b0-156">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="207b0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="207b0-157">CommonParameters</span></span>
<span data-ttu-id="207b0-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="207b0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="207b0-159">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="207b0-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="207b0-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="207b0-160">INPUTS</span></span>

## <span data-ttu-id="207b0-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="207b0-161">OUTPUTS</span></span>

## <span data-ttu-id="207b0-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="207b0-162">NOTES</span></span>

## <span data-ttu-id="207b0-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="207b0-163">RELATED LINKS</span></span>

[<span data-ttu-id="207b0-164">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="207b0-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="207b0-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="207b0-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="207b0-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="207b0-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


