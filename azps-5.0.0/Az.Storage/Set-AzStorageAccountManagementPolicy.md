---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b52dc34ddffb2234962888407ed67c487f4195c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269007"
---
# <span data-ttu-id="a8cd2-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a8cd2-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="a8cd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="a8cd2-103">Skapar eller ändrar hanterings principen för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="a8cd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8cd2-104">SYNTAX</span></span>

### <span data-ttu-id="a8cd2-105">AccountNamePolicyRule (standard)</span><span class="sxs-lookup"><span data-stu-id="a8cd2-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8cd2-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="a8cd2-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8cd2-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a8cd2-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cd2-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a8cd2-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cd2-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a8cd2-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8cd2-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a8cd2-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8cd2-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8cd2-111">DESCRIPTION</span></span>
<span data-ttu-id="a8cd2-112">Cmdleten **set-AzStorageAccountManagementPolicy** skapar eller ändrar hanterings principen för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="a8cd2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8cd2-113">EXAMPLES</span></span>

### <span data-ttu-id="a8cd2-114">Exempel 1: skapa eller uppdatera hanterings principen för ett lagrings konto med ManagementPolicy regel objekt.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="a8cd2-115">Det här kommandot skapar först två ManagementPolicy regel objekt och skapar eller uppdaterar sedan hanterings principen för ett lagrings konto med de två ManagementPolicy-regel objekt.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="a8cd2-116">Exempel 2: skapa eller uppdatera hanterings principen för ett lagrings konto med en JSON-formatering.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled=$true;
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=30};
                    TierToArchive=@{DaysAfterModificationGreaterThan=50};
                    Delete=@{DaysAfterModificationGreaterThan=100};
                });
                Snapshot=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled=$false;
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=80};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  30
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterModificationGreaterThan":  50
                                                                                                   },
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            }
                                                                             }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  false,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="a8cd2-117">Det här kommandot skapar eller uppdaterar hanterings principen för ett lagrings konto med en JSON-format princip.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="a8cd2-118">Exempel 3: Hämta hanterings principen från ett lagrings konto och ange det till ett annat lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="a8cd2-119">Det här kommandot får först en hanterings princip från ett lagrings konto och anger det till ett annat lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="a8cd2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8cd2-120">PARAMETERS</span></span>

### <span data-ttu-id="a8cd2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8cd2-121">-DefaultProfile</span></span>
<span data-ttu-id="a8cd2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8cd2-123">-Princip</span><span class="sxs-lookup"><span data-stu-id="a8cd2-123">-Policy</span></span>
<span data-ttu-id="a8cd2-124">Hanterings princip objekt som ska anges</span><span class="sxs-lookup"><span data-stu-id="a8cd2-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8cd2-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8cd2-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-127">-Regel</span><span class="sxs-lookup"><span data-stu-id="a8cd2-127">-Rule</span></span>
<span data-ttu-id="a8cd2-128">Regler för hanterings principer.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-128">The Management Policy rules.</span></span> <span data-ttu-id="a8cd2-129">Hämta objektet med New-AzStorageAccountManagementPolicyRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8cd2-130">-StorageAccount</span></span>
<span data-ttu-id="a8cd2-131">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="a8cd2-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8cd2-132">-StorageAccountName</span></span>
<span data-ttu-id="a8cd2-133">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a8cd2-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="a8cd2-135">Resurs-ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8cd2-136">-Confirm</span></span>
<span data-ttu-id="a8cd2-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8cd2-138">-WhatIf</span></span>
<span data-ttu-id="a8cd2-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8cd2-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8cd2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8cd2-141">CommonParameters</span></span>
<span data-ttu-id="a8cd2-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8cd2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8cd2-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8cd2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8cd2-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8cd2-144">INPUTS</span></span>

### <span data-ttu-id="a8cd2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a8cd2-145">System.String</span></span>

## <span data-ttu-id="a8cd2-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8cd2-146">OUTPUTS</span></span>

### <span data-ttu-id="a8cd2-147">Microsoft. Azure. commands. Management. Storage. Models. PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a8cd2-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="a8cd2-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8cd2-148">NOTES</span></span>

## <span data-ttu-id="a8cd2-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8cd2-149">RELATED LINKS</span></span>
